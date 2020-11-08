---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046272"
---
# <span data-ttu-id="b34d0-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="b34d0-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="b34d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b34d0-102">SYNOPSIS</span></span>
<span data-ttu-id="b34d0-103">사용 가능한 모든 웹 사이트 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b34d0-103">Gets all available website locations.</span></span>

## <span data-ttu-id="b34d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b34d0-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b34d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b34d0-105">DESCRIPTION</span></span>
<span data-ttu-id="b34d0-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b34d0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b34d0-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b34d0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b34d0-108">현재 구독에 대해 사용 가능한 모든 웹 사이트 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b34d0-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="b34d0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b34d0-109">EXAMPLES</span></span>

### <span data-ttu-id="b34d0-110">예제 1: 사용 가능한 모든 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="b34d0-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="b34d0-111">이 예제에서는 현재 구독에 사용할 수 있는 모든 웹 사이트 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b34d0-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="b34d0-112">변수</span><span class="sxs-lookup"><span data-stu-id="b34d0-112">PARAMETERS</span></span>

### <span data-ttu-id="b34d0-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="b34d0-113">-Profile</span></span>
<span data-ttu-id="b34d0-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b34d0-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b34d0-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b34d0-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34d0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34d0-116">CommonParameters</span></span>
<span data-ttu-id="b34d0-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b34d0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34d0-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34d0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34d0-119">입력</span><span class="sxs-lookup"><span data-stu-id="b34d0-119">INPUTS</span></span>

## <span data-ttu-id="b34d0-120">출력</span><span class="sxs-lookup"><span data-stu-id="b34d0-120">OUTPUTS</span></span>

## <span data-ttu-id="b34d0-121">상속자</span><span class="sxs-lookup"><span data-stu-id="b34d0-121">NOTES</span></span>

## <span data-ttu-id="b34d0-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b34d0-122">RELATED LINKS</span></span>

[<span data-ttu-id="b34d0-123">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b34d0-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


