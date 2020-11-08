---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045862"
---
# <span data-ttu-id="17c3e-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="17c3e-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="17c3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="17c3e-103">가상 머신 개체에 대 한 정적 VNet IP 주소 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="17c3e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17c3e-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="17c3e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="17c3e-105">DESCRIPTION</span></span>
<span data-ttu-id="17c3e-106">**Set-AzureStaticVNetIP** cmdlet은 가상 머신 개체에 대 한 VNet (정적 가상 네트워크) IP 주소 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="17c3e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="17c3e-107">EXAMPLES</span></span>

### <span data-ttu-id="17c3e-108">예제 1: 가상 컴퓨터와 연결 된 가상 네트워크 IP 주소 설정</span><span class="sxs-lookup"><span data-stu-id="17c3e-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="17c3e-109">첫 번째 명령은 가상 네트워크의 구성 경로를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="17c3e-110">두 번째 명령은 가상 컴퓨터 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="17c3e-111">세 번째 명령은 가상 컴퓨터의 서브넷을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="17c3e-112">네 번째 명령은 가상 컴퓨터의 IP 주소를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="17c3e-113">다섯 번째 명령은 가상 컴퓨터를 사용 하 여 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="17c3e-114">변수</span><span class="sxs-lookup"><span data-stu-id="17c3e-114">PARAMETERS</span></span>

### <span data-ttu-id="17c3e-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="17c3e-115">-InformationAction</span></span>
<span data-ttu-id="17c3e-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="17c3e-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="17c3e-118">하기로</span><span class="sxs-lookup"><span data-stu-id="17c3e-118">Continue</span></span>
- <span data-ttu-id="17c3e-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="17c3e-119">Ignore</span></span>
- <span data-ttu-id="17c3e-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="17c3e-120">Inquire</span></span>
- <span data-ttu-id="17c3e-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="17c3e-121">SilentlyContinue</span></span>
- <span data-ttu-id="17c3e-122">중지가</span><span class="sxs-lookup"><span data-stu-id="17c3e-122">Stop</span></span>
- <span data-ttu-id="17c3e-123">대기</span><span class="sxs-lookup"><span data-stu-id="17c3e-123">Suspend</span></span>

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

### <span data-ttu-id="17c3e-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="17c3e-124">-InformationVariable</span></span>
<span data-ttu-id="17c3e-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="17c3e-126">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="17c3e-126">-IPAddress</span></span>
<span data-ttu-id="17c3e-127">정적 VNet IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17c3e-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="17c3e-128">-Profile</span></span>
<span data-ttu-id="17c3e-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17c3e-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17c3e-131">-VM</span><span class="sxs-lookup"><span data-stu-id="17c3e-131">-VM</span></span>
<span data-ttu-id="17c3e-132">정적 VNet IP 주소를 설정할 영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="17c3e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c3e-133">CommonParameters</span></span>
<span data-ttu-id="17c3e-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17c3e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c3e-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17c3e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c3e-136">입력</span><span class="sxs-lookup"><span data-stu-id="17c3e-136">INPUTS</span></span>

## <span data-ttu-id="17c3e-137">출력</span><span class="sxs-lookup"><span data-stu-id="17c3e-137">OUTPUTS</span></span>

## <span data-ttu-id="17c3e-138">상속자</span><span class="sxs-lookup"><span data-stu-id="17c3e-138">NOTES</span></span>

## <span data-ttu-id="17c3e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17c3e-139">RELATED LINKS</span></span>

[<span data-ttu-id="17c3e-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="17c3e-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="17c3e-141">테스트-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="17c3e-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


