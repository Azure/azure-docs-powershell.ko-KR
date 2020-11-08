---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046549"
---
# <span data-ttu-id="5c948-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="5c948-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="5c948-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c948-102">SYNOPSIS</span></span>
<span data-ttu-id="5c948-103">현재 리소스 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-103">Gets the current resource context.</span></span>

## <span data-ttu-id="5c948-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c948-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5c948-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c948-105">DESCRIPTION</span></span>
<span data-ttu-id="5c948-106">**Get-AzureStorSimpleResourceContext** cmdlet은 현재 리소스 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="5c948-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5c948-107">EXAMPLES</span></span>

### <span data-ttu-id="5c948-108">예제 1: 현재 컨텍스트 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c948-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="5c948-109">첫 번째 명령은 **-Azurestorsimplerazurecmdlet** 을 사용 하 여 Contoso63-Tsqa 라는 리소스로 현재 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="5c948-110">두 번째 명령은 현재 리소스 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="5c948-111">예제 2: 현재 컨텍스트 가져오기 시도</span><span class="sxs-lookup"><span data-stu-id="5c948-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="5c948-112">이 명령은 현재 컨텍스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-112">This command gets the current context.</span></span>
<span data-ttu-id="5c948-113">이 예제에서는 컨텍스트가 설정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-113">In this example, no context has been set.</span></span>
<span data-ttu-id="5c948-114">이 명령은 문제를 설명 하는 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="5c948-115">변수</span><span class="sxs-lookup"><span data-stu-id="5c948-115">PARAMETERS</span></span>

### <span data-ttu-id="5c948-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="5c948-116">-Profile</span></span>
<span data-ttu-id="5c948-117">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-117">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="5c948-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c948-118">CommonParameters</span></span>
<span data-ttu-id="5c948-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c948-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c948-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c948-121">입력</span><span class="sxs-lookup"><span data-stu-id="5c948-121">INPUTS</span></span>

### <span data-ttu-id="5c948-122">않아야</span><span class="sxs-lookup"><span data-stu-id="5c948-122">None</span></span>

## <span data-ttu-id="5c948-123">출력</span><span class="sxs-lookup"><span data-stu-id="5c948-123">OUTPUTS</span></span>

### <span data-ttu-id="5c948-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="5c948-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="5c948-125">이 cmdlet은 **Resourcecontext** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c948-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="5c948-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5c948-126">NOTES</span></span>

## <span data-ttu-id="5c948-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c948-127">RELATED LINKS</span></span>

[<span data-ttu-id="5c948-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="5c948-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="5c948-129">선택-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="5c948-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


