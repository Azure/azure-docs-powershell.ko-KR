---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528964"
---
# <span data-ttu-id="aeba4-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="aeba4-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="aeba4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeba4-102">SYNOPSIS</span></span>
<span data-ttu-id="aeba4-103">자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeba4-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeba4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aeba4-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeba4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aeba4-105">DESCRIPTION</span></span>
<span data-ttu-id="aeba4-106">**AzureRmAutoscaleSetting** Cmdlet은 자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeba4-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="aeba4-107">설정의 이름과이를 할당 받은 리소스 그룹의 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeba4-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="aeba4-108">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aeba4-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="aeba4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="aeba4-109">EXAMPLES</span></span>

## <span data-ttu-id="aeba4-110">변수</span><span class="sxs-lookup"><span data-stu-id="aeba4-110">PARAMETERS</span></span>

### <span data-ttu-id="aeba4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeba4-111">-DefaultProfile</span></span>
<span data-ttu-id="aeba4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aeba4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeba4-113">-이름</span><span class="sxs-lookup"><span data-stu-id="aeba4-113">-Name</span></span>
<span data-ttu-id="aeba4-114">제거할 자동 크기 조정 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeba4-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeba4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeba4-115">-ResourceGroupName</span></span>
<span data-ttu-id="aeba4-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeba4-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeba4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeba4-117">CommonParameters</span></span>
<span data-ttu-id="aeba4-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeba4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeba4-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeba4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeba4-120">입력</span><span class="sxs-lookup"><span data-stu-id="aeba4-120">INPUTS</span></span>

### <span data-ttu-id="aeba4-121">않아야</span><span class="sxs-lookup"><span data-stu-id="aeba4-121">None</span></span>
<span data-ttu-id="aeba4-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aeba4-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aeba4-123">출력</span><span class="sxs-lookup"><span data-stu-id="aeba4-123">OUTPUTS</span></span>

### <span data-ttu-id="aeba4-124">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aeba4-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="aeba4-125">상속자</span><span class="sxs-lookup"><span data-stu-id="aeba4-125">NOTES</span></span>

## <span data-ttu-id="aeba4-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aeba4-126">RELATED LINKS</span></span>

[<span data-ttu-id="aeba4-127">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="aeba4-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="aeba4-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="aeba4-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


