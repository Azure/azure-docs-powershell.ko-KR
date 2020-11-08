---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: ACBE32E5-AA8C-43CA-9FF4-4B59906C6B85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 45d18179fba41d39456a11575fc2041ad4be8557
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046530"
---
# <span data-ttu-id="23100-101">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="23100-101">Get-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="23100-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23100-102">SYNOPSIS</span></span>
<span data-ttu-id="23100-103">입력 이미지 컨텍스트에서 디스크 구성 집합 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23100-103">Gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="23100-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23100-104">SYNTAX</span></span>

```
Get-AzureVMImageDiskConfigSet [[-ImageContext] <OSImageContext>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23100-105">설명은</span><span class="sxs-lookup"><span data-stu-id="23100-105">DESCRIPTION</span></span>
<span data-ttu-id="23100-106">**AzureVMImageDiskConfigSet** cmdlet은 입력 이미지 컨텍스트에서 디스크 구성 집합 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23100-106">The **Get-AzureVMImageDiskConfigSet** cmdlet gets a disk configuration set object from the input image context.</span></span>

## <span data-ttu-id="23100-107">예제의</span><span class="sxs-lookup"><span data-stu-id="23100-107">EXAMPLES</span></span>

### <span data-ttu-id="23100-108">예제 1: 가상 머신에서 디스크 구성 집합 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="23100-108">Example 1: Get a disk configuration set object from a virtual machine</span></span>
```
PS C:\> Get-AzureVMImage -ImageName $Img | Get-AzureVMImageDiskConfigSet
```

<span data-ttu-id="23100-109">이 명령은 가상 머신에서 디스크 구성 집합 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23100-109">This command gets a disk configuration set object from a virtual machine.</span></span>

## <span data-ttu-id="23100-110">변수</span><span class="sxs-lookup"><span data-stu-id="23100-110">PARAMETERS</span></span>

### <span data-ttu-id="23100-111">-ImageContext</span><span class="sxs-lookup"><span data-stu-id="23100-111">-ImageContext</span></span>
<span data-ttu-id="23100-112">가상 컴퓨터 이미지 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23100-112">Specifies the virtual machine image context.</span></span>

```yaml
Type: OSImageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23100-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23100-113">-InformationAction</span></span>
<span data-ttu-id="23100-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23100-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23100-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="23100-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23100-116">하기로</span><span class="sxs-lookup"><span data-stu-id="23100-116">Continue</span></span>
- <span data-ttu-id="23100-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="23100-117">Ignore</span></span>
- <span data-ttu-id="23100-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="23100-118">Inquire</span></span>
- <span data-ttu-id="23100-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23100-119">SilentlyContinue</span></span>
- <span data-ttu-id="23100-120">중지가</span><span class="sxs-lookup"><span data-stu-id="23100-120">Stop</span></span>
- <span data-ttu-id="23100-121">대기</span><span class="sxs-lookup"><span data-stu-id="23100-121">Suspend</span></span>

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

### <span data-ttu-id="23100-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23100-122">-InformationVariable</span></span>
<span data-ttu-id="23100-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23100-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23100-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23100-124">CommonParameters</span></span>
<span data-ttu-id="23100-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23100-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23100-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23100-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23100-127">입력</span><span class="sxs-lookup"><span data-stu-id="23100-127">INPUTS</span></span>

## <span data-ttu-id="23100-128">출력</span><span class="sxs-lookup"><span data-stu-id="23100-128">OUTPUTS</span></span>

### <span data-ttu-id="23100-129">WindowsAzure. ServiceManagement. m m/. m a m 설정</span><span class="sxs-lookup"><span data-stu-id="23100-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="23100-130">상속자</span><span class="sxs-lookup"><span data-stu-id="23100-130">NOTES</span></span>

## <span data-ttu-id="23100-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23100-131">RELATED LINKS</span></span>

[<span data-ttu-id="23100-132">새로운 AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="23100-132">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="23100-133">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="23100-133">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)


