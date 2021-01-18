---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495453"
---
# <span data-ttu-id="a7f4c-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="a7f4c-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="a7f4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f4c-103">이 IotHub가 전환할 수 있는 유효한 모든 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="a7f4c-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7f4c-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7f4c-105">설명</span><span class="sxs-lookup"><span data-stu-id="a7f4c-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f4c-106">이 IotHub가 전환할 수 있는 유효한 모든 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="a7f4c-107">IotHub는 무료 및 유료 SKU 간에 전환할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="a7f4c-108">이렇게 하려는 경우 iothub를 삭제하고 다시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="a7f4c-109">예제</span><span class="sxs-lookup"><span data-stu-id="a7f4c-109">EXAMPLES</span></span>

### <span data-ttu-id="a7f4c-110">예제 1 유효한 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a7f4c-111">"myiothub"라는 IotHub에 대한 모든 SKU 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a7f4c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7f4c-112">PARAMETERS</span></span>

### <span data-ttu-id="a7f4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f4c-113">-DefaultProfile</span></span>
<span data-ttu-id="a7f4c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a7f4c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7f4c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a7f4c-115">-Name</span></span>
<span data-ttu-id="a7f4c-116">IoT Hub의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="a7f4c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f4c-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7f4c-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a7f4c-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a7f4c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f4c-119">CommonParameters</span></span>
<span data-ttu-id="a7f4c-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f4c-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a7f4c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f4c-122">입력</span><span class="sxs-lookup"><span data-stu-id="a7f4c-122">INPUTS</span></span>

### <span data-ttu-id="a7f4c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a7f4c-123">System.String</span></span>

## <span data-ttu-id="a7f4c-124">출력</span><span class="sxs-lookup"><span data-stu-id="a7f4c-124">OUTPUTS</span></span>

### <span data-ttu-id="a7f4c-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="a7f4c-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="a7f4c-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a7f4c-126">NOTES</span></span>

## <span data-ttu-id="a7f4c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7f4c-127">RELATED LINKS</span></span>
