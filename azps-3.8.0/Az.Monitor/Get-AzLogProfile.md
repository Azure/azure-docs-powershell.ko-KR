---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044512"
---
# <span data-ttu-id="89c75-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="89c75-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="89c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c75-102">SYNOPSIS</span></span>
<span data-ttu-id="89c75-103">로그 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89c75-103">Gets a log profile.</span></span>

## <span data-ttu-id="89c75-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89c75-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89c75-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89c75-105">DESCRIPTION</span></span>
<span data-ttu-id="89c75-106">**Get-AzLogProfile** cmdlet은 로그 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89c75-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="89c75-107">예제의</span><span class="sxs-lookup"><span data-stu-id="89c75-107">EXAMPLES</span></span>

## <span data-ttu-id="89c75-108">변수</span><span class="sxs-lookup"><span data-stu-id="89c75-108">PARAMETERS</span></span>

### <span data-ttu-id="89c75-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c75-109">-DefaultProfile</span></span>
<span data-ttu-id="89c75-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="89c75-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89c75-111">-이름</span><span class="sxs-lookup"><span data-stu-id="89c75-111">-Name</span></span>
<span data-ttu-id="89c75-112">가져올 로그 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c75-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="89c75-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c75-113">CommonParameters</span></span>
<span data-ttu-id="89c75-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c75-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c75-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="89c75-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c75-116">입력</span><span class="sxs-lookup"><span data-stu-id="89c75-116">INPUTS</span></span>

### <span data-ttu-id="89c75-117">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89c75-117">System.String</span></span>

## <span data-ttu-id="89c75-118">출력</span><span class="sxs-lookup"><span data-stu-id="89c75-118">OUTPUTS</span></span>

### <span data-ttu-id="89c75-119">Microsoft. a PSLogProfileCollection을 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="89c75-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="89c75-120">상속자</span><span class="sxs-lookup"><span data-stu-id="89c75-120">NOTES</span></span>

## <span data-ttu-id="89c75-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89c75-121">RELATED LINKS</span></span>

[<span data-ttu-id="89c75-122">추가-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="89c75-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="89c75-123">제거-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="89c75-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)

