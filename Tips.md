search index 权限报错，解决办法：
在infra/main.bicep文件中增加：

//update search contrib role id
module searchContribRoleUser2 'core/security/role.bicep' = {
  scope: searchServiceResourceGroup
  name: 'search-contrib-role-user2'
  params: {
    principalId: principalId
    roleDefinitionId: '7ca78c08-252a-4471-8644-bb5ff32d4ba0'
    principalType: 'User'
  }
}

//purge openai service using web portal
1. 搜索Forms Recognizer,Open AI
2. 点击"manage deleted resources"
3. 点击"Purge"
