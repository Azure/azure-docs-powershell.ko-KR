---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
ms.openlocfilehash: 60ba6fbf57fa9e1ac9e25a913fb9755902b56ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215307"
---
# <span data-ttu-id="9b427-101">Get-AzManagedHsmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9b427-101">Get-AzManagedHsmRoleDefinition</span></span>

## <span data-ttu-id="9b427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b427-102">SYNOPSIS</span></span>
<span data-ttu-id="9b427-103">지정 된 범위에서 지정 된 관리 되는 HSM의 역할 정의를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="9b427-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b427-104">SYNTAX</span></span>

### <span data-ttu-id="9b427-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b427-105">Interactive (Default)</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b427-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9b427-106">ByName</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b427-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9b427-107">DESCRIPTION</span></span>
<span data-ttu-id="9b427-108">지정 된 범위에서 지정 된 관리 되는 HSM의 역할 정의를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="9b427-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9b427-109">EXAMPLES</span></span>

### <span data-ttu-id="9b427-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b427-110">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="9b427-111">이 예제에서는 "/keys" 범위의 모든 역할을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="9b427-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="9b427-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzManagedHsmRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="9b427-113">이 예제에서는 "관리 되는 HSM Backup" 역할을 가져와 해당 권한을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="9b427-114">변수</span><span class="sxs-lookup"><span data-stu-id="9b427-114">PARAMETERS</span></span>

### <span data-ttu-id="9b427-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b427-115">-DefaultProfile</span></span>
<span data-ttu-id="9b427-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b427-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="9b427-117">-HsmName</span></span>
<span data-ttu-id="9b427-118">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="9b427-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9b427-119">-RoleDefinitionName</span></span>
<span data-ttu-id="9b427-120">가져올 역할 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b427-121">-범위</span><span class="sxs-lookup"><span data-stu-id="9b427-121">-Scope</span></span>
<span data-ttu-id="9b427-122">역할 할당 또는 정의가 적용 되는 범위 (예: '/' 또는 '/keys ' 또는 '/keys/{keyName} ')입니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="9b427-123">생략 하면 '/'가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="9b427-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b427-124">CommonParameters</span></span>
<span data-ttu-id="9b427-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b427-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b427-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b427-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b427-127">입력</span><span class="sxs-lookup"><span data-stu-id="9b427-127">INPUTS</span></span>

### <span data-ttu-id="9b427-128">않아야</span><span class="sxs-lookup"><span data-stu-id="9b427-128">None</span></span>

## <span data-ttu-id="9b427-129">출력</span><span class="sxs-lookup"><span data-stu-id="9b427-129">OUTPUTS</span></span>

### <span data-ttu-id="9b427-130">Microsoft. KeyVault. PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9b427-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="9b427-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9b427-131">NOTES</span></span>

## <span data-ttu-id="9b427-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b427-132">RELATED LINKS</span></span>
