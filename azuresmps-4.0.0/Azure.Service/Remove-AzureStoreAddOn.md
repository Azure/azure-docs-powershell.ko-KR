---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046455"
---
# <span data-ttu-id="69d64-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="69d64-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="69d64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69d64-102">SYNOPSIS</span></span>
<span data-ttu-id="69d64-103">기존 추가 기능 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="69d64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69d64-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="69d64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69d64-105">DESCRIPTION</span></span>
<span data-ttu-id="69d64-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="69d64-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="69d64-108">현재 구독에서 기존 추가 기능 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="69d64-109">예제의</span><span class="sxs-lookup"><span data-stu-id="69d64-109">EXAMPLES</span></span>

### <span data-ttu-id="69d64-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="69d64-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="69d64-111">이 예제에서는 현재 구독에서 MyAddOn 이라는 추가 기능을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="69d64-112">변수</span><span class="sxs-lookup"><span data-stu-id="69d64-112">PARAMETERS</span></span>

### <span data-ttu-id="69d64-113">-이름</span><span class="sxs-lookup"><span data-stu-id="69d64-113">-Name</span></span>
<span data-ttu-id="69d64-114">제거할 추가 기능 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-114">Specifies the name of the add-on instance to remove.</span></span>

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

### <span data-ttu-id="69d64-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69d64-115">-PassThru</span></span>
<span data-ttu-id="69d64-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69d64-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69d64-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="69d64-118">-Profile</span></span>
<span data-ttu-id="69d64-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69d64-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69d64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69d64-121">CommonParameters</span></span>
<span data-ttu-id="69d64-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69d64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69d64-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69d64-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69d64-124">입력</span><span class="sxs-lookup"><span data-stu-id="69d64-124">INPUTS</span></span>

## <span data-ttu-id="69d64-125">출력</span><span class="sxs-lookup"><span data-stu-id="69d64-125">OUTPUTS</span></span>

## <span data-ttu-id="69d64-126">상속자</span><span class="sxs-lookup"><span data-stu-id="69d64-126">NOTES</span></span>

## <span data-ttu-id="69d64-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69d64-127">RELATED LINKS</span></span>

[<span data-ttu-id="69d64-128">Get-Azure프로젝트 추가 기능</span><span class="sxs-lookup"><span data-stu-id="69d64-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="69d64-129">새-Azure추가 기능</span><span class="sxs-lookup"><span data-stu-id="69d64-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="69d64-130">Set-Azure기능 추가 기능</span><span class="sxs-lookup"><span data-stu-id="69d64-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


