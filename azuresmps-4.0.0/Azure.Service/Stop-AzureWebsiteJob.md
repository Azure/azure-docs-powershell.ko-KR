---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045838"
---
# <span data-ttu-id="57f86-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="57f86-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="57f86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f86-102">SYNOPSIS</span></span>
<span data-ttu-id="57f86-103">웹사이트의 웹 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="57f86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57f86-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="57f86-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57f86-105">DESCRIPTION</span></span>
<span data-ttu-id="57f86-106">**AzureWebsiteJob** cmdlet은 웹사이트에 대 한 웹 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="57f86-107">예제의</span><span class="sxs-lookup"><span data-stu-id="57f86-107">EXAMPLES</span></span>

### <span data-ttu-id="57f86-108">예제 1: 웹 사이트에 대 한 웹 작업 중지</span><span class="sxs-lookup"><span data-stu-id="57f86-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="57f86-109">MyWebSite 용 MyWebJob 이라는 웹 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="57f86-110">변수</span><span class="sxs-lookup"><span data-stu-id="57f86-110">PARAMETERS</span></span>

### <span data-ttu-id="57f86-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="57f86-111">-JobName</span></span>
<span data-ttu-id="57f86-112">웹 작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-112">The web job name.</span></span>

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

### <span data-ttu-id="57f86-113">-이름</span><span class="sxs-lookup"><span data-stu-id="57f86-113">-Name</span></span>
<span data-ttu-id="57f86-114">Azure 웹 사이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-114">The name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f86-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57f86-115">-PassThru</span></span>
<span data-ttu-id="57f86-116">작업이 성공적으로 중지 되었음을 나타내는 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="57f86-117">기본적으로이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-117">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f86-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="57f86-118">-Profile</span></span>
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

### <span data-ttu-id="57f86-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="57f86-119">-Slot</span></span>
<span data-ttu-id="57f86-120">Azure 웹 사이트의 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-120">The slot name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f86-121">CommonParameters</span></span>
<span data-ttu-id="57f86-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f86-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57f86-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f86-124">입력</span><span class="sxs-lookup"><span data-stu-id="57f86-124">INPUTS</span></span>

## <span data-ttu-id="57f86-125">출력</span><span class="sxs-lookup"><span data-stu-id="57f86-125">OUTPUTS</span></span>

## <span data-ttu-id="57f86-126">상속자</span><span class="sxs-lookup"><span data-stu-id="57f86-126">NOTES</span></span>

## <span data-ttu-id="57f86-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57f86-127">RELATED LINKS</span></span>

[<span data-ttu-id="57f86-128">중지-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="57f86-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="57f86-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="57f86-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="57f86-130">새로운 AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="57f86-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="57f86-131">제거-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="57f86-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="57f86-132">시작-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="57f86-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


