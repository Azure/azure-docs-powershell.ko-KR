---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1c4395c4e2c36fd07fee6345c1a5ff7d724b7c0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975744"
---
# <span data-ttu-id="5e5d7-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5e5d7-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="5e5d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5d7-103">새 사용자 할당 ID를 생성하거나 기존 사용자 할당 ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="5e5d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="5e5d7-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e5d7-105">설명</span><span class="sxs-lookup"><span data-stu-id="5e5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="5e5d7-106">**New-AzUserAssignedIdentity** cmdlet은 새 사용자 할당 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="5e5d7-107">기존 ID와 함께 사용하는 경우 ID가 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="5e5d7-108">ID에 Azure Resource Manager 태그를 추가하기 위해 Set-AzResource cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="5e5d7-109">예제</span><span class="sxs-lookup"><span data-stu-id="5e5d7-109">EXAMPLES</span></span>

### <span data-ttu-id="5e5d7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5e5d7-110">Example 1</span></span>
<span data-ttu-id="5e5d7-111">이 예제 cmdlet은 ResourceGroup의 위치에 리소스 그룹 **PSRG** 아래에 이름 **ID1이** 있는 새 사용자 할당 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="5e5d7-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="5e5d7-112">Example 2</span></span>
<span data-ttu-id="5e5d7-113">이 예제 cmdlet은 서부 지역의 리소스 그룹 **PSRG** 아래에 이름 **ID1이** 있는 새 사용자 할당 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="5e5d7-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5e5d7-114">PARAMETERS</span></span>

### <span data-ttu-id="5e5d7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e5d7-115">-AsJob</span></span>
<span data-ttu-id="5e5d7-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5e5d7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e5d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e5d7-117">-DefaultProfile</span></span>
<span data-ttu-id="5e5d7-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e5d7-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5e5d7-119">-Location</span></span>
<span data-ttu-id="5e5d7-120">ID를 만들어야 하는 Azure 지역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5d7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5e5d7-121">-Name</span></span>
<span data-ttu-id="5e5d7-122">ID 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e5d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e5d7-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5d7-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e5d7-125">-Tag</span></span>
<span data-ttu-id="5e5d7-126">ID와 연결된 Azure Resource Manager 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e5d7-127">-확인</span><span class="sxs-lookup"><span data-stu-id="5e5d7-127">-Confirm</span></span>
<span data-ttu-id="5e5d7-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e5d7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e5d7-129">-WhatIf</span></span>
<span data-ttu-id="5e5d7-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e5d7-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e5d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5d7-132">CommonParameters</span></span>
<span data-ttu-id="5e5d7-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5d7-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5e5d7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5d7-135">입력</span><span class="sxs-lookup"><span data-stu-id="5e5d7-135">INPUTS</span></span>

### <span data-ttu-id="5e5d7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5e5d7-136">System.String</span></span>

### <span data-ttu-id="5e5d7-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e5d7-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5e5d7-138">출력</span><span class="sxs-lookup"><span data-stu-id="5e5d7-138">OUTPUTS</span></span>

### <span data-ttu-id="5e5d7-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5e5d7-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="5e5d7-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5e5d7-140">NOTES</span></span>

## <span data-ttu-id="5e5d7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e5d7-141">RELATED LINKS</span></span>
