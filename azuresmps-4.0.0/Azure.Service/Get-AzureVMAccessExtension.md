---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 734C98C1-0EF7-43E5-AB6F-A1C625FF9CE7
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9713c8b39fa4e2842cdf1cfcbfe962ead86d729
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045535"
---
# <span data-ttu-id="40236-101">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="40236-101">Get-AzureVMAccessExtension</span></span>

## <span data-ttu-id="40236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40236-102">SYNOPSIS</span></span>
<span data-ttu-id="40236-103">가상 컴퓨터에 적용 된 VMAccess 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40236-103">Gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="40236-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40236-104">SYNTAX</span></span>

```
Get-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="40236-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40236-105">DESCRIPTION</span></span>
<span data-ttu-id="40236-106">**AzureVMAccessExtension** cmdlet은 가상 컴퓨터에 적용 되는 vmaccess 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40236-106">The **Get-AzureVMAccessExtension** cmdlet gets the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="40236-107">예제의</span><span class="sxs-lookup"><span data-stu-id="40236-107">EXAMPLES</span></span>

### <span data-ttu-id="40236-108">예제 1: 가상 컴퓨터에 대 한 VMAccess 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="40236-108">Example 1: Get the VMAccess extension for a virtual machine</span></span>
```
PS C:\> Get-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="40236-109">이 명령은 가상 컴퓨터에 대 한 VMAccess 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40236-109">This command gets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="40236-110">변수</span><span class="sxs-lookup"><span data-stu-id="40236-110">PARAMETERS</span></span>

### <span data-ttu-id="40236-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="40236-111">-InformationAction</span></span>
<span data-ttu-id="40236-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40236-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="40236-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="40236-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="40236-114">하기로</span><span class="sxs-lookup"><span data-stu-id="40236-114">Continue</span></span>
- <span data-ttu-id="40236-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="40236-115">Ignore</span></span>
- <span data-ttu-id="40236-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="40236-116">Inquire</span></span>
- <span data-ttu-id="40236-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="40236-117">SilentlyContinue</span></span>
- <span data-ttu-id="40236-118">중지가</span><span class="sxs-lookup"><span data-stu-id="40236-118">Stop</span></span>
- <span data-ttu-id="40236-119">대기</span><span class="sxs-lookup"><span data-stu-id="40236-119">Suspend</span></span>

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

### <span data-ttu-id="40236-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="40236-120">-InformationVariable</span></span>
<span data-ttu-id="40236-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40236-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="40236-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="40236-122">-Profile</span></span>
<span data-ttu-id="40236-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40236-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40236-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="40236-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40236-125">-VM</span><span class="sxs-lookup"><span data-stu-id="40236-125">-VM</span></span>
<span data-ttu-id="40236-126">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40236-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="40236-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40236-127">CommonParameters</span></span>
<span data-ttu-id="40236-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40236-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40236-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40236-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40236-130">입력</span><span class="sxs-lookup"><span data-stu-id="40236-130">INPUTS</span></span>

## <span data-ttu-id="40236-131">출력</span><span class="sxs-lookup"><span data-stu-id="40236-131">OUTPUTS</span></span>

## <span data-ttu-id="40236-132">상속자</span><span class="sxs-lookup"><span data-stu-id="40236-132">NOTES</span></span>

## <span data-ttu-id="40236-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40236-133">RELATED LINKS</span></span>

[<span data-ttu-id="40236-134">제거-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="40236-134">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)

[<span data-ttu-id="40236-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="40236-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


