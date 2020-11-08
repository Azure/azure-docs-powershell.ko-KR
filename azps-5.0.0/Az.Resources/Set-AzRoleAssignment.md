---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226526"
---
# Set-AzRoleAssignment

## SYNOPSIS
기존 역할 과제를 업데이트 합니다.

## 구문과

### RoleAssignmentParameterSet (기본값)
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputFileParameterSet
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
New-AzRoleAssignment 명령을 사용 하 여 기존 과제를 수정할 수 있습니다.  
설명은 유효한 문자열일 수 있으며,이를 사용 하 여 서로를 diferentiate.  
조건이 설정 된 경우에도 조건 버전을 설정 해야 하지만 필요 하지 않은 조건을 업데이트 하는 경우
조건 버전을 1.0에서 2.0로 업그레이드할 수 있지만 다시 다운 그레이드할 수는 없습니다. 2.0는 1.0와 retrocompatible 되지 않기 때문에 주의를 기울여야 합니다.

## 예제의

### 예제 1
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

개체를 수정 하 여 기존 역할 할당 업데이트

### 예제 2
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

파일을 사용 하 여 기존 역할 할당 업데이트

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputFile
단일 역할 정의를 포함 하는 파일 이름입니다.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
역할 할당.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
지정 된 경우 업데이트 된 역할 할당을 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### .Resources. PSRoleAssignment를 할당 합니다.

## 출력

### .Resources. PSRoleAssignment를 할당 합니다.

## 상속자

## 관련 링크
