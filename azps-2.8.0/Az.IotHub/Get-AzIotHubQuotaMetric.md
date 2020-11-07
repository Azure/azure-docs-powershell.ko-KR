---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 6d8ea34de1520326ead270ffa44837388729bc5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689732"
---
# <span data-ttu-id="60458-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="60458-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="60458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60458-102">SYNOPSIS</span></span>
<span data-ttu-id="60458-103">IotHub의 할당량 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60458-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="60458-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60458-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60458-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60458-105">DESCRIPTION</span></span>
<span data-ttu-id="60458-106">IotHub의 할당량 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60458-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="60458-107">예제의</span><span class="sxs-lookup"><span data-stu-id="60458-107">EXAMPLES</span></span>

### <span data-ttu-id="60458-108">예제 1 할당량 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="60458-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="60458-109">"Myiothub" IotHub에 대 한 할당량 메트릭 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="60458-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="60458-110">변수</span><span class="sxs-lookup"><span data-stu-id="60458-110">PARAMETERS</span></span>

### <span data-ttu-id="60458-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60458-111">-DefaultProfile</span></span>
<span data-ttu-id="60458-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60458-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60458-113">-이름</span><span class="sxs-lookup"><span data-stu-id="60458-113">-Name</span></span>
<span data-ttu-id="60458-114">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60458-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="60458-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60458-115">-ResourceGroupName</span></span>
<span data-ttu-id="60458-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="60458-116">Resource Group Name</span></span>

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

### <span data-ttu-id="60458-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60458-117">CommonParameters</span></span>
<span data-ttu-id="60458-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60458-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60458-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60458-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60458-120">입력</span><span class="sxs-lookup"><span data-stu-id="60458-120">INPUTS</span></span>

### <span data-ttu-id="60458-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60458-121">System.String</span></span>

## <span data-ttu-id="60458-122">출력</span><span class="sxs-lookup"><span data-stu-id="60458-122">OUTPUTS</span></span>

### <span data-ttu-id="60458-123">IotHub. PSIotHubQuotaMetric/. \*</span><span class="sxs-lookup"><span data-stu-id="60458-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="60458-124">상속자</span><span class="sxs-lookup"><span data-stu-id="60458-124">NOTES</span></span>

## <span data-ttu-id="60458-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60458-125">RELATED LINKS</span></span>
