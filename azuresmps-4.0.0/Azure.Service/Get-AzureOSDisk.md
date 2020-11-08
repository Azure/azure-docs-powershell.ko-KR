---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046332"
---
# <span data-ttu-id="e7121-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="e7121-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="e7121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7121-102">SYNOPSIS</span></span>
<span data-ttu-id="e7121-103">Azure 가상 컴퓨터의 운영 체제 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="e7121-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7121-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7121-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7121-105">DESCRIPTION</span></span>
<span data-ttu-id="e7121-106">**AzureOSDisk** Cmdlet은 Azure 가상 컴퓨터의 운영 체제 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="e7121-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7121-107">EXAMPLES</span></span>

### <span data-ttu-id="e7121-108">예제 1: 운영 체제 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="e7121-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="e7121-109">이 명령은 VirtualMachine02 cmdlet을 사용 하 여 ContosoService 이라는 서비스의 가상 컴퓨터 (이름 = **)** 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="e7121-110">이 명령은 파이프라인 연산자를 사용 하 여 가상 컴퓨터를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e7121-111">현재 cmdlet은 해당 가상 컴퓨터의 운영 체제 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="e7121-112">변수</span><span class="sxs-lookup"><span data-stu-id="e7121-112">PARAMETERS</span></span>

### <span data-ttu-id="e7121-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e7121-113">-InformationAction</span></span>
<span data-ttu-id="e7121-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e7121-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7121-116">하기로</span><span class="sxs-lookup"><span data-stu-id="e7121-116">Continue</span></span>
- <span data-ttu-id="e7121-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="e7121-117">Ignore</span></span>
- <span data-ttu-id="e7121-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="e7121-118">Inquire</span></span>
- <span data-ttu-id="e7121-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e7121-119">SilentlyContinue</span></span>
- <span data-ttu-id="e7121-120">중지가</span><span class="sxs-lookup"><span data-stu-id="e7121-120">Stop</span></span>
- <span data-ttu-id="e7121-121">대기</span><span class="sxs-lookup"><span data-stu-id="e7121-121">Suspend</span></span>

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

### <span data-ttu-id="e7121-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e7121-122">-InformationVariable</span></span>
<span data-ttu-id="e7121-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e7121-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="e7121-124">-Profile</span></span>
<span data-ttu-id="e7121-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7121-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7121-127">-VM</span><span class="sxs-lookup"><span data-stu-id="e7121-127">-VM</span></span>
<span data-ttu-id="e7121-128">이 cmdlet이 운영 체제 디스크를 가져오는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="e7121-129">가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="e7121-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7121-130">CommonParameters</span></span>
<span data-ttu-id="e7121-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7121-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7121-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7121-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7121-133">입력</span><span class="sxs-lookup"><span data-stu-id="e7121-133">INPUTS</span></span>

## <span data-ttu-id="e7121-134">출력</span><span class="sxs-lookup"><span data-stu-id="e7121-134">OUTPUTS</span></span>

## <span data-ttu-id="e7121-135">상속자</span><span class="sxs-lookup"><span data-stu-id="e7121-135">NOTES</span></span>

## <span data-ttu-id="e7121-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7121-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7121-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="e7121-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="e7121-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="e7121-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


