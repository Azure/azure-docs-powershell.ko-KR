---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045508"
---
# <span data-ttu-id="fce82-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="fce82-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="fce82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fce82-102">SYNOPSIS</span></span>
<span data-ttu-id="fce82-103">가상 컴퓨터에 적용 된 BGInfo 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fce82-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fce82-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fce82-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fce82-105">DESCRIPTION</span></span>
<span data-ttu-id="fce82-106">**AzureVMBGInfoExtension** cmdlet은 가상 컴퓨터에 적용 된 BGInfo 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fce82-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fce82-107">EXAMPLES</span></span>

### <span data-ttu-id="fce82-108">예제 1: 가상 컴퓨터에서 BGInfo 확장 제거</span><span class="sxs-lookup"><span data-stu-id="fce82-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="fce82-109">이 명령은 가상 컴퓨터에 적용 된 BGInfo 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="fce82-110">변수</span><span class="sxs-lookup"><span data-stu-id="fce82-110">PARAMETERS</span></span>

### <span data-ttu-id="fce82-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fce82-111">-InformationAction</span></span>
<span data-ttu-id="fce82-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fce82-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fce82-114">하기로</span><span class="sxs-lookup"><span data-stu-id="fce82-114">Continue</span></span>
- <span data-ttu-id="fce82-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="fce82-115">Ignore</span></span>
- <span data-ttu-id="fce82-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="fce82-116">Inquire</span></span>
- <span data-ttu-id="fce82-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fce82-117">SilentlyContinue</span></span>
- <span data-ttu-id="fce82-118">중지가</span><span class="sxs-lookup"><span data-stu-id="fce82-118">Stop</span></span>
- <span data-ttu-id="fce82-119">대기</span><span class="sxs-lookup"><span data-stu-id="fce82-119">Suspend</span></span>

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

### <span data-ttu-id="fce82-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fce82-120">-InformationVariable</span></span>
<span data-ttu-id="fce82-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fce82-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="fce82-122">-Profile</span></span>
<span data-ttu-id="fce82-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fce82-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fce82-125">-VM</span><span class="sxs-lookup"><span data-stu-id="fce82-125">-VM</span></span>
<span data-ttu-id="fce82-126">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="fce82-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce82-127">CommonParameters</span></span>
<span data-ttu-id="fce82-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fce82-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce82-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce82-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce82-130">입력</span><span class="sxs-lookup"><span data-stu-id="fce82-130">INPUTS</span></span>

## <span data-ttu-id="fce82-131">출력</span><span class="sxs-lookup"><span data-stu-id="fce82-131">OUTPUTS</span></span>

## <span data-ttu-id="fce82-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fce82-132">NOTES</span></span>

## <span data-ttu-id="fce82-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fce82-133">RELATED LINKS</span></span>

[<span data-ttu-id="fce82-134">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="fce82-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="fce82-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="fce82-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


