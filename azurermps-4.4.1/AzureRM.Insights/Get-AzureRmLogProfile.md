---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: 2964b95dcaba44ba57d354951eb5ccfb4ea9ef6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703730"
---
# <span data-ttu-id="6eba8-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6eba8-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="6eba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eba8-102">SYNOPSIS</span></span>
<span data-ttu-id="6eba8-103">로그 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6eba8-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eba8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6eba8-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eba8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6eba8-105">DESCRIPTION</span></span>
<span data-ttu-id="6eba8-106">**Get-AzureRmLogProfile** cmdlet은 로그 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6eba8-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="6eba8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6eba8-107">EXAMPLES</span></span>

## <span data-ttu-id="6eba8-108">변수</span><span class="sxs-lookup"><span data-stu-id="6eba8-108">PARAMETERS</span></span>

### <span data-ttu-id="6eba8-109">-이름</span><span class="sxs-lookup"><span data-stu-id="6eba8-109">-Name</span></span>
<span data-ttu-id="6eba8-110">가져올 로그 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba8-110">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="6eba8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eba8-111">-DefaultProfile</span></span>
<span data-ttu-id="6eba8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6eba8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eba8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eba8-113">CommonParameters</span></span>
<span data-ttu-id="6eba8-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eba8-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eba8-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eba8-116">입력</span><span class="sxs-lookup"><span data-stu-id="6eba8-116">INPUTS</span></span>

## <span data-ttu-id="6eba8-117">출력</span><span class="sxs-lookup"><span data-stu-id="6eba8-117">OUTPUTS</span></span>

### <span data-ttu-id="6eba8-118">Microsoft. a PSLogProfileCollection을 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba8-118">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="6eba8-119">상속자</span><span class="sxs-lookup"><span data-stu-id="6eba8-119">NOTES</span></span>

## <span data-ttu-id="6eba8-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eba8-120">RELATED LINKS</span></span>

[<span data-ttu-id="6eba8-121">추가-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6eba8-121">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="6eba8-122">제거-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6eba8-122">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


