---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: d6ee5a3acfd2cfafb66f0517f21f087b7a8550e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536652"
---
# <span data-ttu-id="3c0a6-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3c0a6-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="3c0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0a6-103">로그 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3c0a6-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c0a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3c0a6-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c0a6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3c0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="3c0a6-106">**Get-AzureRmLogProfile** cmdlet은 로그 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3c0a6-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="3c0a6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3c0a6-107">EXAMPLES</span></span>

## <span data-ttu-id="3c0a6-108">변수</span><span class="sxs-lookup"><span data-stu-id="3c0a6-108">PARAMETERS</span></span>

### <span data-ttu-id="3c0a6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0a6-109">-DefaultProfile</span></span>
<span data-ttu-id="3c0a6-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3c0a6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c0a6-111">-이름</span><span class="sxs-lookup"><span data-stu-id="3c0a6-111">-Name</span></span>
<span data-ttu-id="3c0a6-112">가져올 로그 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c0a6-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="3c0a6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0a6-113">CommonParameters</span></span>
<span data-ttu-id="3c0a6-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c0a6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0a6-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c0a6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0a6-116">입력</span><span class="sxs-lookup"><span data-stu-id="3c0a6-116">INPUTS</span></span>

### <span data-ttu-id="3c0a6-117">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3c0a6-117">System.String</span></span>

## <span data-ttu-id="3c0a6-118">출력</span><span class="sxs-lookup"><span data-stu-id="3c0a6-118">OUTPUTS</span></span>

### <span data-ttu-id="3c0a6-119">Microsoft. a PSLogProfileCollection을 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3c0a6-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="3c0a6-120">상속자</span><span class="sxs-lookup"><span data-stu-id="3c0a6-120">NOTES</span></span>

## <span data-ttu-id="3c0a6-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c0a6-121">RELATED LINKS</span></span>

[<span data-ttu-id="3c0a6-122">추가-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3c0a6-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="3c0a6-123">제거-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3c0a6-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


