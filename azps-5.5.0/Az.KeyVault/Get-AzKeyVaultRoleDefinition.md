---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: 6e4f58c355296a281a9ecbef21d7eca754bf41c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188164"
---
# <span data-ttu-id="a889b-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a889b-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="a889b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a889b-102">SYNOPSIS</span></span>
<span data-ttu-id="a889b-103">지정한 범위에서 관리되는 HSM의 역할 정의를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="a889b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a889b-104">SYNTAX</span></span>

### <span data-ttu-id="a889b-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="a889b-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a889b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a889b-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a889b-107">설명</span><span class="sxs-lookup"><span data-stu-id="a889b-107">DESCRIPTION</span></span>
<span data-ttu-id="a889b-108">지정한 범위에서 관리되는 HSM의 역할 정의를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="a889b-109">예제</span><span class="sxs-lookup"><span data-stu-id="a889b-109">EXAMPLES</span></span>

### <span data-ttu-id="a889b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a889b-110">Example 1</span></span>
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

<span data-ttu-id="a889b-111">이 예제에서는 "/keys" 범위의 모든 역할을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="a889b-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a889b-112">Example 2</span></span>
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

<span data-ttu-id="a889b-113">이 예제에서는 "관리되는 HSM Backup" 역할을 수행하고 해당 권한을 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="a889b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a889b-114">PARAMETERS</span></span>

### <span data-ttu-id="a889b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a889b-115">-DefaultProfile</span></span>
<span data-ttu-id="a889b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a889b-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a889b-117">-HsmName</span></span>
<span data-ttu-id="a889b-118">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="a889b-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a889b-119">-RoleDefinitionName</span></span>
<span data-ttu-id="a889b-120">얻을 역할 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="a889b-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="a889b-121">-Scope</span></span>
<span data-ttu-id="a889b-122">역할 할당 또는 정의가 적용되는 범위입니다(예: '/' 또는 '/keys' 또는 '/keys/{keyName}').</span><span class="sxs-lookup"><span data-stu-id="a889b-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="a889b-123">'/'는 생략할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="a889b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a889b-124">CommonParameters</span></span>
<span data-ttu-id="a889b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a889b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a889b-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a889b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a889b-127">입력</span><span class="sxs-lookup"><span data-stu-id="a889b-127">INPUTS</span></span>

### <span data-ttu-id="a889b-128">없음</span><span class="sxs-lookup"><span data-stu-id="a889b-128">None</span></span>

## <span data-ttu-id="a889b-129">출력</span><span class="sxs-lookup"><span data-stu-id="a889b-129">OUTPUTS</span></span>

### <span data-ttu-id="a889b-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a889b-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="a889b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a889b-131">NOTES</span></span>

## <span data-ttu-id="a889b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a889b-132">RELATED LINKS</span></span>
