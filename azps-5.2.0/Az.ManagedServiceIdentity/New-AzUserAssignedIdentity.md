---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 1f165177871a2d8b425829dddaef6d1f0298cfb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356903"
---
# <span data-ttu-id="a0c7c-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a0c7c-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="a0c7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c7c-103">새 사용자 할당 ID를 생성하거나 기존 사용자 할당 ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="a0c7c-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0c7c-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0c7c-105">설명</span><span class="sxs-lookup"><span data-stu-id="a0c7c-105">DESCRIPTION</span></span>
<span data-ttu-id="a0c7c-106">**New-AzUserAssignedIdentity** cmdlet은 새 사용자 할당 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="a0c7c-107">기존 ID와 함께 사용하는 경우 ID를 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="a0c7c-108">ID에 Azure Resource Manager 태그를 추가하기 위해 Set-AzResource cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="a0c7c-109">예제</span><span class="sxs-lookup"><span data-stu-id="a0c7c-109">EXAMPLES</span></span>

### <span data-ttu-id="a0c7c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a0c7c-110">Example 1</span></span>
<span data-ttu-id="a0c7c-111">이 예제 cmdlet은 ResourceGroup의 위치에 있는 리소스 그룹 **PSRG** 아래에 이름 **ID1이** 있는 새 사용자 할당 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

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

### <span data-ttu-id="a0c7c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a0c7c-112">Example 2</span></span>
<span data-ttu-id="a0c7c-113">이 예제 cmdlet은 westus 지역의 리소스 그룹 **PSRG** 아래에 이름 **ID1이** 있는 새 사용자 할당 ID를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

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

## <span data-ttu-id="a0c7c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0c7c-114">PARAMETERS</span></span>

### <span data-ttu-id="a0c7c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0c7c-115">-AsJob</span></span>
<span data-ttu-id="a0c7c-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a0c7c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0c7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c7c-117">-DefaultProfile</span></span>
<span data-ttu-id="a0c7c-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0c7c-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a0c7c-119">-Location</span></span>
<span data-ttu-id="a0c7c-120">ID를 만들어야 하는 Azure 지역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-120">The Azure region name where the Identity should be created.</span></span>

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

### <span data-ttu-id="a0c7c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a0c7c-121">-Name</span></span>
<span data-ttu-id="a0c7c-122">ID 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-122">The Identity name.</span></span>

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

### <span data-ttu-id="a0c7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0c7c-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-124">The resource group name.</span></span>

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

### <span data-ttu-id="a0c7c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0c7c-125">-Tag</span></span>
<span data-ttu-id="a0c7c-126">ID와 연결된 Azure Resource Manager 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-126">The Azure Resource Manager tags associated with the identity.</span></span>

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

### <span data-ttu-id="a0c7c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0c7c-127">-Confirm</span></span>
<span data-ttu-id="a0c7c-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0c7c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0c7c-129">-WhatIf</span></span>
<span data-ttu-id="a0c7c-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a0c7c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0c7c-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0c7c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c7c-132">CommonParameters</span></span>
<span data-ttu-id="a0c7c-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c7c-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a0c7c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c7c-135">입력</span><span class="sxs-lookup"><span data-stu-id="a0c7c-135">INPUTS</span></span>

### <span data-ttu-id="a0c7c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a0c7c-136">System.String</span></span>

### <span data-ttu-id="a0c7c-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a0c7c-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a0c7c-138">출력</span><span class="sxs-lookup"><span data-stu-id="a0c7c-138">OUTPUTS</span></span>

### <span data-ttu-id="a0c7c-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a0c7c-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="a0c7c-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0c7c-140">NOTES</span></span>

## <span data-ttu-id="a0c7c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0c7c-141">RELATED LINKS</span></span>
