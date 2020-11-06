---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534071"
---
# <span data-ttu-id="bfd75-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bfd75-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="bfd75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfd75-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd75-103">자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd75-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfd75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bfd75-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfd75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bfd75-105">DESCRIPTION</span></span>
<span data-ttu-id="bfd75-106">**AzureRmAutoscaleSetting** Cmdlet은 자동 크기 조정 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd75-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="bfd75-107">설정의 이름과이를 할당 받은 리소스 그룹의 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd75-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="bfd75-108">예제의</span><span class="sxs-lookup"><span data-stu-id="bfd75-108">EXAMPLES</span></span>

## <span data-ttu-id="bfd75-109">변수</span><span class="sxs-lookup"><span data-stu-id="bfd75-109">PARAMETERS</span></span>

### <span data-ttu-id="bfd75-110">-이름</span><span class="sxs-lookup"><span data-stu-id="bfd75-110">-Name</span></span>
<span data-ttu-id="bfd75-111">제거할 자동 크기 조정 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd75-111">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="bfd75-112">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bfd75-112">-ResourceGroup</span></span>
<span data-ttu-id="bfd75-113">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd75-113">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bfd75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd75-114">-DefaultProfile</span></span>
<span data-ttu-id="bfd75-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfd75-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfd75-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd75-116">CommonParameters</span></span>
<span data-ttu-id="bfd75-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfd75-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd75-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfd75-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd75-119">입력</span><span class="sxs-lookup"><span data-stu-id="bfd75-119">INPUTS</span></span>

## <span data-ttu-id="bfd75-120">출력</span><span class="sxs-lookup"><span data-stu-id="bfd75-120">OUTPUTS</span></span>

### <span data-ttu-id="bfd75-121">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bfd75-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="bfd75-122">상속자</span><span class="sxs-lookup"><span data-stu-id="bfd75-122">NOTES</span></span>

## <span data-ttu-id="bfd75-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfd75-123">RELATED LINKS</span></span>

[<span data-ttu-id="bfd75-124">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bfd75-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="bfd75-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="bfd75-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


