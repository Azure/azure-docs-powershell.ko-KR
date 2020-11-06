---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529535"
---
# <span data-ttu-id="f18c3-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f18c3-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="f18c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f18c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f18c3-103">리소스 그룹 또는 구독에서 가상 WAN 또는 모든 가상 Wan을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f18c3-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f18c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f18c3-104">SYNTAX</span></span>

### <span data-ttu-id="f18c3-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="f18c3-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f18c3-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f18c3-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f18c3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f18c3-107">DESCRIPTION</span></span>
<span data-ttu-id="f18c3-108">리소스 그룹 또는 구독에서 가상 WAN 또는 모든 가상 Wan을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f18c3-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="f18c3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f18c3-109">EXAMPLES</span></span>

### <span data-ttu-id="f18c3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f18c3-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="f18c3-111">이 명령은 리소스 그룹 testRG에서 myVirtualWAN 이라는 가상 WAN을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f18c3-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="f18c3-112">변수</span><span class="sxs-lookup"><span data-stu-id="f18c3-112">PARAMETERS</span></span>

### <span data-ttu-id="f18c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f18c3-113">-DefaultProfile</span></span>
<span data-ttu-id="f18c3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f18c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f18c3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f18c3-115">-Name</span></span>
<span data-ttu-id="f18c3-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f18c3-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f18c3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f18c3-117">-ResourceGroupName</span></span>
<span data-ttu-id="f18c3-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f18c3-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f18c3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f18c3-119">CommonParameters</span></span>
<span data-ttu-id="f18c3-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f18c3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f18c3-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f18c3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f18c3-122">입력</span><span class="sxs-lookup"><span data-stu-id="f18c3-122">INPUTS</span></span>

### <span data-ttu-id="f18c3-123">않아야</span><span class="sxs-lookup"><span data-stu-id="f18c3-123">None</span></span>

## <span data-ttu-id="f18c3-124">출력</span><span class="sxs-lookup"><span data-stu-id="f18c3-124">OUTPUTS</span></span>

### <span data-ttu-id="f18c3-125">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="f18c3-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="f18c3-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f18c3-126">NOTES</span></span>

## <span data-ttu-id="f18c3-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f18c3-127">RELATED LINKS</span></span>
