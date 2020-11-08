---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045543"
---
# <span data-ttu-id="f52bb-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="f52bb-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="f52bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f52bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f52bb-103">지정 된 Azure 가상 컴퓨터와 연결 된 서브넷 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="f52bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f52bb-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f52bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f52bb-105">DESCRIPTION</span></span>
<span data-ttu-id="f52bb-106">**AzureSubnet** cmdlet은 지정 된 가상 컴퓨터와 연결 된 서브넷 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="f52bb-107">**Get-help** 를 사용 하 여 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="f52bb-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f52bb-108">EXAMPLES</span></span>

### <span data-ttu-id="f52bb-109">예제 1: 가상 컴퓨터용 서브넷 가져오기</span><span class="sxs-lookup"><span data-stu-id="f52bb-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="f52bb-110">첫 번째 명령은 ContosoService03 이라는 서비스에서 VirtualMachine01 이라는 가상 컴퓨터를 가져온 다음이를 $VM 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="f52bb-111">두 번째 명령은 $VM에서 가상 컴퓨터에 대 한 Azure 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="f52bb-112">변수</span><span class="sxs-lookup"><span data-stu-id="f52bb-112">PARAMETERS</span></span>

### <span data-ttu-id="f52bb-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f52bb-113">-InformationAction</span></span>
<span data-ttu-id="f52bb-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f52bb-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f52bb-116">하기로</span><span class="sxs-lookup"><span data-stu-id="f52bb-116">Continue</span></span>
- <span data-ttu-id="f52bb-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="f52bb-117">Ignore</span></span>
- <span data-ttu-id="f52bb-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="f52bb-118">Inquire</span></span>
- <span data-ttu-id="f52bb-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f52bb-119">SilentlyContinue</span></span>
- <span data-ttu-id="f52bb-120">중지가</span><span class="sxs-lookup"><span data-stu-id="f52bb-120">Stop</span></span>
- <span data-ttu-id="f52bb-121">대기</span><span class="sxs-lookup"><span data-stu-id="f52bb-121">Suspend</span></span>

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

### <span data-ttu-id="f52bb-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f52bb-122">-InformationVariable</span></span>
<span data-ttu-id="f52bb-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f52bb-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="f52bb-124">-Profile</span></span>
<span data-ttu-id="f52bb-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f52bb-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f52bb-127">-VM</span><span class="sxs-lookup"><span data-stu-id="f52bb-127">-VM</span></span>
<span data-ttu-id="f52bb-128">서브넷 목록을 가져올 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

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

### <span data-ttu-id="f52bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52bb-129">CommonParameters</span></span>
<span data-ttu-id="f52bb-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f52bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52bb-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52bb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52bb-132">입력</span><span class="sxs-lookup"><span data-stu-id="f52bb-132">INPUTS</span></span>

## <span data-ttu-id="f52bb-133">출력</span><span class="sxs-lookup"><span data-stu-id="f52bb-133">OUTPUTS</span></span>

## <span data-ttu-id="f52bb-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f52bb-134">NOTES</span></span>

## <span data-ttu-id="f52bb-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f52bb-135">RELATED LINKS</span></span>

[<span data-ttu-id="f52bb-136">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f52bb-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f52bb-137">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="f52bb-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


