---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045951"
---
# <span data-ttu-id="09d7b-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="09d7b-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="09d7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="09d7b-103">Azure 가상 컴퓨터에 대 한 서브넷 목록을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="09d7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09d7b-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="09d7b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="09d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="09d7b-106">**AzureSubnet** cmdlet은 가상 컴퓨터 구성에 대 한 서브넷 목록을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="09d7b-107">**뉴욕** 에서 사용 하 여 가상 컴퓨터용 서브넷을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="09d7b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="09d7b-108">EXAMPLES</span></span>

### <span data-ttu-id="09d7b-109">예제 1: 가상 컴퓨터 구성에 서브넷 추가</span><span class="sxs-lookup"><span data-stu-id="09d7b-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="09d7b-110">이 명령은 가상 컴퓨터 구성에 서브넷을 추가한 다음 VirtualMachine04 이라는 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="09d7b-111">변수</span><span class="sxs-lookup"><span data-stu-id="09d7b-111">PARAMETERS</span></span>

### <span data-ttu-id="09d7b-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="09d7b-112">-InformationAction</span></span>
<span data-ttu-id="09d7b-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="09d7b-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09d7b-115">하기로</span><span class="sxs-lookup"><span data-stu-id="09d7b-115">Continue</span></span>
- <span data-ttu-id="09d7b-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="09d7b-116">Ignore</span></span>
- <span data-ttu-id="09d7b-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="09d7b-117">Inquire</span></span>
- <span data-ttu-id="09d7b-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="09d7b-118">SilentlyContinue</span></span>
- <span data-ttu-id="09d7b-119">중지가</span><span class="sxs-lookup"><span data-stu-id="09d7b-119">Stop</span></span>
- <span data-ttu-id="09d7b-120">대기</span><span class="sxs-lookup"><span data-stu-id="09d7b-120">Suspend</span></span>

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

### <span data-ttu-id="09d7b-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="09d7b-121">-InformationVariable</span></span>
<span data-ttu-id="09d7b-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="09d7b-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="09d7b-123">-Profile</span></span>
<span data-ttu-id="09d7b-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="09d7b-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="09d7b-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="09d7b-126">-SubnetNames</span></span>
<span data-ttu-id="09d7b-127">서브넷 이름 목록을 포함 하는 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d7b-128">-VM</span><span class="sxs-lookup"><span data-stu-id="09d7b-128">-VM</span></span>
<span data-ttu-id="09d7b-129">가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-129">Specifies the virtual machine object.</span></span>

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

### <span data-ttu-id="09d7b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d7b-130">CommonParameters</span></span>
<span data-ttu-id="09d7b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d7b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d7b-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d7b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d7b-133">입력</span><span class="sxs-lookup"><span data-stu-id="09d7b-133">INPUTS</span></span>

## <span data-ttu-id="09d7b-134">출력</span><span class="sxs-lookup"><span data-stu-id="09d7b-134">OUTPUTS</span></span>

## <span data-ttu-id="09d7b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="09d7b-135">NOTES</span></span>

## <span data-ttu-id="09d7b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09d7b-136">RELATED LINKS</span></span>

[<span data-ttu-id="09d7b-137">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="09d7b-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="09d7b-138">뉴욕</span><span class="sxs-lookup"><span data-stu-id="09d7b-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="09d7b-139">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="09d7b-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


