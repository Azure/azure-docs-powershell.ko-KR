---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046545"
---
# <span data-ttu-id="625e6-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="625e6-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="625e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="625e6-102">SYNOPSIS</span></span>
<span data-ttu-id="625e6-103">가상 컴퓨터에 적용 된 요리사 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="625e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="625e6-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="625e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="625e6-105">DESCRIPTION</span></span>
<span data-ttu-id="625e6-106">**AzureVMChefExtension** cmdlet은 가상 컴퓨터에 적용 된 요리사 extension을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="625e6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="625e6-107">EXAMPLES</span></span>

### <span data-ttu-id="625e6-108">예제 1: 지정 된 가상 컴퓨터에 적용 된 요리사 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="625e6-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="625e6-109">이 명령은 지정 된 가상 컴퓨터에 적용 된 요리사 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="625e6-110">변수</span><span class="sxs-lookup"><span data-stu-id="625e6-110">PARAMETERS</span></span>

### <span data-ttu-id="625e6-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="625e6-111">-InformationAction</span></span>
<span data-ttu-id="625e6-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="625e6-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="625e6-114">하기로</span><span class="sxs-lookup"><span data-stu-id="625e6-114">Continue</span></span>
- <span data-ttu-id="625e6-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="625e6-115">Ignore</span></span>
- <span data-ttu-id="625e6-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="625e6-116">Inquire</span></span>
- <span data-ttu-id="625e6-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="625e6-117">SilentlyContinue</span></span>
- <span data-ttu-id="625e6-118">중지가</span><span class="sxs-lookup"><span data-stu-id="625e6-118">Stop</span></span>
- <span data-ttu-id="625e6-119">대기</span><span class="sxs-lookup"><span data-stu-id="625e6-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625e6-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="625e6-120">-InformationVariable</span></span>
<span data-ttu-id="625e6-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625e6-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="625e6-122">-Profile</span></span>
<span data-ttu-id="625e6-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="625e6-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="625e6-125">-VM</span><span class="sxs-lookup"><span data-stu-id="625e6-125">-VM</span></span>
<span data-ttu-id="625e6-126">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-126">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="625e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625e6-127">CommonParameters</span></span>
<span data-ttu-id="625e6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="625e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625e6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="625e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625e6-130">입력</span><span class="sxs-lookup"><span data-stu-id="625e6-130">INPUTS</span></span>

## <span data-ttu-id="625e6-131">출력</span><span class="sxs-lookup"><span data-stu-id="625e6-131">OUTPUTS</span></span>

## <span data-ttu-id="625e6-132">상속자</span><span class="sxs-lookup"><span data-stu-id="625e6-132">NOTES</span></span>

## <span data-ttu-id="625e6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="625e6-133">RELATED LINKS</span></span>

[<span data-ttu-id="625e6-134">제거-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="625e6-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="625e6-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="625e6-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


