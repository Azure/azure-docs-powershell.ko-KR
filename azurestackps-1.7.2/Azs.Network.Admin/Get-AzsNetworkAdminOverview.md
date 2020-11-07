---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874303"
---
# <span data-ttu-id="fc60c-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="fc60c-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="fc60c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc60c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc60c-103">네트워크 리소스 공급자의 상태에 대 한 개요를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc60c-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="fc60c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc60c-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="fc60c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fc60c-105">DESCRIPTION</span></span>
<span data-ttu-id="fc60c-106">네트워크 리소스 공급자의 상태에 대 한 개요를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc60c-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="fc60c-107">개별 속성은 리소스 사용 및 구성 요소의 상태에 대 한 자세한 개수를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc60c-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="fc60c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fc60c-108">EXAMPLES</span></span>

### <span data-ttu-id="fc60c-109">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc60c-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="fc60c-110">네트워크 관리 개요를 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="fc60c-110">Get network admin overview.</span></span>

### <span data-ttu-id="fc60c-111">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc60c-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="fc60c-112">공용 ip 주소 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fc60c-112">Get public ip address usage.</span></span>

## <span data-ttu-id="fc60c-113">변수</span><span class="sxs-lookup"><span data-stu-id="fc60c-113">PARAMETERS</span></span>

### <span data-ttu-id="fc60c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc60c-114">CommonParameters</span></span>
<span data-ttu-id="fc60c-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc60c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc60c-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc60c-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc60c-117">입력</span><span class="sxs-lookup"><span data-stu-id="fc60c-117">INPUTS</span></span>

## <span data-ttu-id="fc60c-118">출력</span><span class="sxs-lookup"><span data-stu-id="fc60c-118">OUTPUTS</span></span>

### <span data-ttu-id="fc60c-119">Microsoft AzureStack. 관리자. 관리 모델 개요</span><span class="sxs-lookup"><span data-stu-id="fc60c-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="fc60c-120">상속자</span><span class="sxs-lookup"><span data-stu-id="fc60c-120">NOTES</span></span>

## <span data-ttu-id="fc60c-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc60c-121">RELATED LINKS</span></span>

