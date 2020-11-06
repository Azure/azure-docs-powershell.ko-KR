---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528516"
---
# <span data-ttu-id="8a160-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8a160-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="8a160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a160-102">SYNOPSIS</span></span>
<span data-ttu-id="8a160-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="8a160-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a160-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a160-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a160-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a160-105">DESCRIPTION</span></span>
<span data-ttu-id="8a160-106">**Get-AzureRmServiceEndpointPolicy** cmdlet은 서비스 끝점 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a160-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="8a160-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a160-107">EXAMPLES</span></span>

### <span data-ttu-id="8a160-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a160-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8a160-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ServiceEndpointPolicy1 이라는 이름의 서비스 끝점 정책을 가져오고이를 $policy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a160-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="8a160-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="8a160-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8a160-111">이 명령은 ResourceGroup01 이라는 리소스 그룹에 있는 모든 서비스 끝점 정책의 목록을 가져와이를 $policyList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a160-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="8a160-112">변수</span><span class="sxs-lookup"><span data-stu-id="8a160-112">PARAMETERS</span></span>

### <span data-ttu-id="8a160-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a160-113">-DefaultProfile</span></span>
<span data-ttu-id="8a160-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a160-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a160-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8a160-115">-Name</span></span>
<span data-ttu-id="8a160-116">서비스 끝점 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a160-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a160-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a160-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a160-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a160-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a160-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a160-119">CommonParameters</span></span>
<span data-ttu-id="8a160-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a160-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8a160-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a160-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a160-122">입력</span><span class="sxs-lookup"><span data-stu-id="8a160-122">INPUTS</span></span>

### <span data-ttu-id="8a160-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a160-123">System.String</span></span>


## <span data-ttu-id="8a160-124">출력</span><span class="sxs-lookup"><span data-stu-id="8a160-124">OUTPUTS</span></span>

### <span data-ttu-id="8a160-125">Microsoft. 네트워크. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8a160-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="8a160-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8a160-126">NOTES</span></span>

## <span data-ttu-id="8a160-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a160-127">RELATED LINKS</span></span>
