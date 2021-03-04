---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: b5d5da8c02081437f064fc1d2a6a29a5b772e8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001435"
---
# <span data-ttu-id="fedbe-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fedbe-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="fedbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fedbe-102">SYNOPSIS</span></span>
<span data-ttu-id="fedbe-103">주어진 범위에서 관리되는 HSM의 역할 정의를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="fedbe-104">구문</span><span class="sxs-lookup"><span data-stu-id="fedbe-104">SYNTAX</span></span>

### <span data-ttu-id="fedbe-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="fedbe-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fedbe-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fedbe-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fedbe-107">설명</span><span class="sxs-lookup"><span data-stu-id="fedbe-107">DESCRIPTION</span></span>
<span data-ttu-id="fedbe-108">주어진 범위에서 관리되는 HSM의 역할 정의를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="fedbe-109">예제</span><span class="sxs-lookup"><span data-stu-id="fedbe-109">EXAMPLES</span></span>

### <span data-ttu-id="fedbe-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fedbe-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

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

<span data-ttu-id="fedbe-111">이 예제에서는 "/keys" 범위의 모든 역할을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="fedbe-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="fedbe-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

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

<span data-ttu-id="fedbe-113">이 예제에서는 "관리형 HSM Backup" 역할을 얻게 하여 해당 권한을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="fedbe-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fedbe-114">PARAMETERS</span></span>

### <span data-ttu-id="fedbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fedbe-115">-DefaultProfile</span></span>
<span data-ttu-id="fedbe-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fedbe-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="fedbe-117">-HsmName</span></span>
<span data-ttu-id="fedbe-118">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="fedbe-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fedbe-119">-RoleDefinitionName</span></span>
<span data-ttu-id="fedbe-120">얻을 역할 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="fedbe-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="fedbe-121">-Scope</span></span>
<span data-ttu-id="fedbe-122">역할 할당 또는 정의가 적용되는 범위(예: '/' 또는 '/key' 또는 '/key/{keyName}').</span><span class="sxs-lookup"><span data-stu-id="fedbe-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="fedbe-123">'/'는 생략할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="fedbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fedbe-124">CommonParameters</span></span>
<span data-ttu-id="fedbe-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fedbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fedbe-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fedbe-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fedbe-127">입력</span><span class="sxs-lookup"><span data-stu-id="fedbe-127">INPUTS</span></span>

### <span data-ttu-id="fedbe-128">없음</span><span class="sxs-lookup"><span data-stu-id="fedbe-128">None</span></span>

## <span data-ttu-id="fedbe-129">출력</span><span class="sxs-lookup"><span data-stu-id="fedbe-129">OUTPUTS</span></span>

### <span data-ttu-id="fedbe-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="fedbe-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="fedbe-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fedbe-131">NOTES</span></span>

## <span data-ttu-id="fedbe-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fedbe-132">RELATED LINKS</span></span>
