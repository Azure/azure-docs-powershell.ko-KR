---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046348"
---
# <span data-ttu-id="24ee1-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="24ee1-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="24ee1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="24ee1-103">IP 전달 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="24ee1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24ee1-104">SYNTAX</span></span>

### <span data-ttu-id="24ee1-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="24ee1-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="24ee1-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="24ee1-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="24ee1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="24ee1-107">DESCRIPTION</span></span>
<span data-ttu-id="24ee1-108">**Get-AzureIPForwarding 전환** CMDLET은 IP 전달의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="24ee1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="24ee1-109">EXAMPLES</span></span>

### <span data-ttu-id="24ee1-110">예제 1: 가상 컴퓨터의 IP 전달 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="24ee1-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="24ee1-111">이 명령은 ContosoService 이라는 서비스에 대 한 ContosoVM06 이라는 가상 컴퓨터를 가져오고 현재 cmdlet에 해당 가상 컴퓨터 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="24ee1-112">현재 cmdlet은 해당 가상 컴퓨터에 대 한 IP 전달 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="24ee1-113">변수</span><span class="sxs-lookup"><span data-stu-id="24ee1-113">PARAMETERS</span></span>

### <span data-ttu-id="24ee1-114">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="24ee1-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="24ee1-115">이 cmdlet이 IP 전달 상태를 가져오는 네트워크 어댑터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

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

### <span data-ttu-id="24ee1-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="24ee1-116">-Profile</span></span>
<span data-ttu-id="24ee1-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="24ee1-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="24ee1-119">-RoleName</span><span class="sxs-lookup"><span data-stu-id="24ee1-119">-RoleName</span></span>
<span data-ttu-id="24ee1-120">이 cmdlet이 IP 전달 상태를 가져오는 PaaS 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ee1-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="24ee1-121">-ServiceName</span></span>
<span data-ttu-id="24ee1-122">클라우드 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="24ee1-123">PaaS 역할은이 매개 변수에서 지정 하는 서비스에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="24ee1-124">-슬롯</span><span class="sxs-lookup"><span data-stu-id="24ee1-124">-Slot</span></span>
<span data-ttu-id="24ee1-125">PaaS 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="24ee1-126">이 cmdlet이 착신 전환 하는 데 사용할 PaaS 역할에는이 매개 변수에서 지정 하는 슬롯이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="24ee1-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-127">Valid values are:</span></span> 

- <span data-ttu-id="24ee1-128">프로덕션용</span><span class="sxs-lookup"><span data-stu-id="24ee1-128">Production</span></span>
- <span data-ttu-id="24ee1-129">대기</span><span class="sxs-lookup"><span data-stu-id="24ee1-129">Staging</span></span> 

<span data-ttu-id="24ee1-130">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ee1-131">-VM</span><span class="sxs-lookup"><span data-stu-id="24ee1-131">-VM</span></span>
<span data-ttu-id="24ee1-132">이 cmdlet이 IP 전달 상태를 가져오는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24ee1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ee1-133">CommonParameters</span></span>
<span data-ttu-id="24ee1-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24ee1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ee1-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ee1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ee1-136">입력</span><span class="sxs-lookup"><span data-stu-id="24ee1-136">INPUTS</span></span>

## <span data-ttu-id="24ee1-137">출력</span><span class="sxs-lookup"><span data-stu-id="24ee1-137">OUTPUTS</span></span>

### <span data-ttu-id="24ee1-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24ee1-138">System.String</span></span>

## <span data-ttu-id="24ee1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="24ee1-139">NOTES</span></span>

## <span data-ttu-id="24ee1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24ee1-140">RELATED LINKS</span></span>

[<span data-ttu-id="24ee1-141">Set-AzureIPForwarding 전환</span><span class="sxs-lookup"><span data-stu-id="24ee1-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


