---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 572e3d61f4d7cf514cc44fe965a7726288806a9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689408"
---
# <span data-ttu-id="3dc40-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3dc40-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="3dc40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dc40-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc40-103">새 사용자에 게 할당 된 Id를 만들거나 기존 사용자에 게 할당 된 Id를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="3dc40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3dc40-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc40-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3dc40-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc40-106">**AzUserAssignedIdentity** cmdlet은 새 사용자 지정 id를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="3dc40-107">이미 기존 id와 함께 사용 하면 id를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="3dc40-108">Azure 리소스 관리자 태그를 id에 추가 하려면 Set-AzResource cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="3dc40-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="3dc40-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3dc40-109">EXAMPLES</span></span>

### <span data-ttu-id="3dc40-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3dc40-110">Example 1</span></span>
<span data-ttu-id="3dc40-111">이 예제 cmdlet은 ResourceGroup의 위치에 있는 리소스 그룹 **Psrg** 아래에서 이름이 **ID1** 인 새 사용자 할당 id를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

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

### <span data-ttu-id="3dc40-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="3dc40-112">Example 2</span></span>
<span data-ttu-id="3dc40-113">이 예제 cmdlet은 westus 지역의 리소스 그룹 **Psrg** 아래에서 이름이 **ID1** 인 새 사용자 할당 id를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

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

## <span data-ttu-id="3dc40-114">변수</span><span class="sxs-lookup"><span data-stu-id="3dc40-114">PARAMETERS</span></span>

### <span data-ttu-id="3dc40-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dc40-115">-AsJob</span></span>
<span data-ttu-id="3dc40-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3dc40-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dc40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc40-117">-DefaultProfile</span></span>
<span data-ttu-id="3dc40-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dc40-119">-위치</span><span class="sxs-lookup"><span data-stu-id="3dc40-119">-Location</span></span>
<span data-ttu-id="3dc40-120">Id를 만들어야 하는 Azure 지역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-120">The Azure region name where the Identity should be created.</span></span>

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

### <span data-ttu-id="3dc40-121">-이름</span><span class="sxs-lookup"><span data-stu-id="3dc40-121">-Name</span></span>
<span data-ttu-id="3dc40-122">Id 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-122">The Identity name.</span></span>

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

### <span data-ttu-id="3dc40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc40-123">-ResourceGroupName</span></span>
<span data-ttu-id="3dc40-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-124">The resource group name.</span></span>

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

### <span data-ttu-id="3dc40-125">태그</span><span class="sxs-lookup"><span data-stu-id="3dc40-125">-Tag</span></span>
<span data-ttu-id="3dc40-126">Id와 연결 된 Azure Resource Manager 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-126">The Azure Resource Manager tags associated with the identity.</span></span>

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

### <span data-ttu-id="3dc40-127">-확인</span><span class="sxs-lookup"><span data-stu-id="3dc40-127">-Confirm</span></span>
<span data-ttu-id="3dc40-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc40-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc40-129">-WhatIf</span></span>
<span data-ttu-id="3dc40-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc40-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc40-132">CommonParameters</span></span>
<span data-ttu-id="3dc40-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3dc40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc40-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc40-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc40-135">입력</span><span class="sxs-lookup"><span data-stu-id="3dc40-135">INPUTS</span></span>

### <span data-ttu-id="3dc40-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3dc40-136">System.String</span></span>

### <span data-ttu-id="3dc40-137">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="3dc40-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3dc40-138">출력</span><span class="sxs-lookup"><span data-stu-id="3dc40-138">OUTPUTS</span></span>

### <span data-ttu-id="3dc40-139">ManagedServiceIdentity. PsUserAssignedIdentity/.</span><span class="sxs-lookup"><span data-stu-id="3dc40-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="3dc40-140">상속자</span><span class="sxs-lookup"><span data-stu-id="3dc40-140">NOTES</span></span>

## <span data-ttu-id="3dc40-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3dc40-141">RELATED LINKS</span></span>
