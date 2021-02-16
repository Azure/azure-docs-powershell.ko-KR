---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/get-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Get-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Get-AzUserAssignedIdentity.md
ms.openlocfilehash: 293c7c54147c254f7cf2f34ffdb2ffbe1f865b09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190268"
---
# <span data-ttu-id="13197-101">Get-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="13197-101">Get-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="13197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13197-102">SYNOPSIS</span></span>
<span data-ttu-id="13197-103">사용자 할당 ID/ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13197-103">Gets User Assigned Identity/identities.</span></span>

## <span data-ttu-id="13197-104">구문</span><span class="sxs-lookup"><span data-stu-id="13197-104">SYNTAX</span></span>

### <span data-ttu-id="13197-105">SuscriptionParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="13197-105">SuscriptionParameterSet (Default)</span></span>
```
Get-AzUserAssignedIdentity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13197-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="13197-106">ResourceGroupParameterSet</span></span>
```
Get-AzUserAssignedIdentity -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13197-107">설명</span><span class="sxs-lookup"><span data-stu-id="13197-107">DESCRIPTION</span></span>
<span data-ttu-id="13197-108">**Get-AzUserAssignedIdentity는** 기존 사용자 할당 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13197-108">The **Get-AzUserAssignedIdentity** gets existing user assigned identities.</span></span>

## <span data-ttu-id="13197-109">예제</span><span class="sxs-lookup"><span data-stu-id="13197-109">EXAMPLES</span></span>

### <span data-ttu-id="13197-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="13197-110">Example 1</span></span>
<span data-ttu-id="13197-111">이 예제 cmdlet은 리소스 그룹 PSRG에서 이름 **ID1이** 있는 사용자 할당 ID를 **얻습니다.**</span><span class="sxs-lookup"><span data-stu-id="13197-111">This example cmdlet gets the User Assigned Identity with name **ID1** under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

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

### <span data-ttu-id="13197-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="13197-112">Example 2</span></span>
<span data-ttu-id="13197-113">이 예제 cmdlet은 리소스 그룹 PSRG에서 모든 사용자 할당 ID를 **얻습니다.**</span><span class="sxs-lookup"><span data-stu-id="13197-113">This example cmdlet gets all the User Assigned Identities under the resource group **PSRG**</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity -ResourceGroupName PSRG

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="13197-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="13197-114">Example 3</span></span>
<span data-ttu-id="13197-115">이 예제 cmdlet은 구독에서 모든 사용자 할당 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13197-115">This example cmdlet gets all the User Assigned Identities under the subscription.</span></span>

```powershell
PS C:\> Get-AzUserAssignedIdentity

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2

ResourceGroupName : PSRG

Name              : ID2

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID2/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities


Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG2

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG2/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="13197-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13197-116">PARAMETERS</span></span>

### <span data-ttu-id="13197-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13197-117">-DefaultProfile</span></span>
<span data-ttu-id="13197-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13197-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13197-119">-Name</span><span class="sxs-lookup"><span data-stu-id="13197-119">-Name</span></span>
<span data-ttu-id="13197-120">ID 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13197-120">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13197-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13197-121">-ResourceGroupName</span></span>
<span data-ttu-id="13197-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13197-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13197-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13197-123">CommonParameters</span></span>
<span data-ttu-id="13197-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13197-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13197-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13197-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13197-126">입력</span><span class="sxs-lookup"><span data-stu-id="13197-126">INPUTS</span></span>

### <span data-ttu-id="13197-127">System.String</span><span class="sxs-lookup"><span data-stu-id="13197-127">System.String</span></span>

## <span data-ttu-id="13197-128">출력</span><span class="sxs-lookup"><span data-stu-id="13197-128">OUTPUTS</span></span>

### <span data-ttu-id="13197-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="13197-129">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="13197-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13197-130">NOTES</span></span>

## <span data-ttu-id="13197-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13197-131">RELATED LINKS</span></span>
