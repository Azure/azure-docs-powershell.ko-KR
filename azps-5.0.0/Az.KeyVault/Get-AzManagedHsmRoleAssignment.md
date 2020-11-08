---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 20e80617d47cd0a1f0ffb5cdb80d836656cd9abd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215306"
---
# Get-AzManagedHsmRoleAssignment

## SYNOPSIS
관리 되는 HSM의 역할 할당을 가져오거나 나열 합니다. 해당 매개 변수를 사용 하 여 특정 사용자 또는 역할 정의에 대 한 과제를 나열 합니다.

## 구문과

### 목록 (기본값)
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByName
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
명령을 사용 `Get-AzManagedHsmRoleAssignment` 하 여 범위에 적용 되는 모든 역할 과제를 나열 합니다.
매개 변수 없이이 명령은 관리 되는 HSM에서 생성 된 모든 역할 과제를 반환 합니다.
이 목록은 주도자, 역할 및 범위에 대 한 필터링 매개 변수를 사용 하 여 필터링 할 수 있습니다.
과제의 주제를 지정 해야 합니다.
사용자를 지정 하려면 SignInName 또는 Azure AD ObjectId 매개 변수를 사용 합니다.
보안 그룹을 지정 하려면 Azure AD ObjectId 매개 변수를 사용 합니다.
Azure AD 응용 프로그램을 지정 하려면 ApplicationId 또는 ObjectId 매개 변수를 사용 합니다.
지정 되는 역할은 RoleDefinitionName 또는 RoleDefinitionId 매개 변수를 사용 하 여 지정 해야 합니다.
액세스가 허용 되는 범위를 지정할 수 있습니다. 기본값은 "/"입니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

이 예제에서는 모든 범위에서 "myHsm"의 모든 역할 지정을 나열 합니다.

### 예제 2
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

이 예제에서는 "/keys" 범위에서 "myHsm"의 모든 역할 지정을 나열 하 고 사용자 로그인 이름으로 결과를 필터링 합니다.

## 변수

### -ApplicationId
앱 SPN.

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -HsmName
HSM의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
사용자 또는 그룹 개체 id입니다.

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleAssignmentName
역할 할당의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionId
주도자가 지정 된 역할 Id입니다.

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionName
사용자에 게 할당할 RBAC 역할의 이름입니다.

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -범위
역할 할당 또는 정의가 적용 되는 범위 (예: '/' 또는 '/keys ' 또는 '/keys/{keyName} ')입니다.
생략 하면 '/'가 사용 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInName
사용자 SignInName.

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### Microsoft. KeyVault. PSKeyVaultRoleAssignment

## 상속자

## 관련 링크
