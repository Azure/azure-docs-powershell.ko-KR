---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: d1c52cef6548f8762f972789a1fd9d47e8cc92aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711104"
---
# <span data-ttu-id="e344f-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="e344f-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="e344f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e344f-102">SYNOPSIS</span></span>
<span data-ttu-id="e344f-103">이 IotHub 전환할 수 있는 유효한 모든 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e344f-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e344f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e344f-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e344f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e344f-105">DESCRIPTION</span></span>
<span data-ttu-id="e344f-106">이 IotHub 전환할 수 있는 유효한 모든 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e344f-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="e344f-107">IotHub는 무료 및 유료 sku 간에 전환할 수 없으며 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="e344f-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="e344f-108">이 작업을 수행 하려면 iothub를 삭제 하 고 다시 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e344f-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="e344f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e344f-109">EXAMPLES</span></span>

### <span data-ttu-id="e344f-110">예제 1 유효한 sku 구하기</span><span class="sxs-lookup"><span data-stu-id="e344f-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e344f-111">"Myiothub" IotHub에 대 한 모든 sku 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e344f-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e344f-112">변수</span><span class="sxs-lookup"><span data-stu-id="e344f-112">PARAMETERS</span></span>

### <span data-ttu-id="e344f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e344f-113">-DefaultProfile</span></span>
<span data-ttu-id="e344f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e344f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e344f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e344f-115">-Name</span></span>
<span data-ttu-id="e344f-116">IoT hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e344f-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="e344f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e344f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e344f-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e344f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e344f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e344f-119">CommonParameters</span></span>
<span data-ttu-id="e344f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e344f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e344f-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e344f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e344f-122">입력</span><span class="sxs-lookup"><span data-stu-id="e344f-122">INPUTS</span></span>

### <span data-ttu-id="e344f-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e344f-123">System.String</span></span>

## <span data-ttu-id="e344f-124">출력</span><span class="sxs-lookup"><span data-stu-id="e344f-124">OUTPUTS</span></span>

### <span data-ttu-id="e344f-125">IotHub. PSIotHubSkuDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="e344f-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="e344f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e344f-126">NOTES</span></span>

## <span data-ttu-id="e344f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e344f-127">RELATED LINKS</span></span>
