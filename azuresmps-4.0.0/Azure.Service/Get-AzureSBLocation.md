---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046312"
---
# <span data-ttu-id="50a1d-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="50a1d-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="50a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="50a1d-103">서비스 버스의 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50a1d-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="50a1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50a1d-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="50a1d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50a1d-105">DESCRIPTION</span></span>
<span data-ttu-id="50a1d-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a1d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="50a1d-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a1d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="50a1d-108">**Get-AzureSBLocation** Cmdlet은 서비스 버스를 사용할 수 있는 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a1d-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="50a1d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="50a1d-109">EXAMPLES</span></span>

### <span data-ttu-id="50a1d-110">예제 1: 서비스 버스 위치 가져오기</span><span class="sxs-lookup"><span data-stu-id="50a1d-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="50a1d-111">이 예제에서는 서비스 버스의 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50a1d-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="50a1d-112">변수</span><span class="sxs-lookup"><span data-stu-id="50a1d-112">PARAMETERS</span></span>

### <span data-ttu-id="50a1d-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="50a1d-113">-Profile</span></span>
<span data-ttu-id="50a1d-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a1d-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50a1d-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="50a1d-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50a1d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a1d-116">CommonParameters</span></span>
<span data-ttu-id="50a1d-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50a1d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a1d-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50a1d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a1d-119">입력</span><span class="sxs-lookup"><span data-stu-id="50a1d-119">INPUTS</span></span>

## <span data-ttu-id="50a1d-120">출력</span><span class="sxs-lookup"><span data-stu-id="50a1d-120">OUTPUTS</span></span>

## <span data-ttu-id="50a1d-121">상속자</span><span class="sxs-lookup"><span data-stu-id="50a1d-121">NOTES</span></span>

## <span data-ttu-id="50a1d-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50a1d-122">RELATED LINKS</span></span>

[<span data-ttu-id="50a1d-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="50a1d-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)


