---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046582"
---
# <span data-ttu-id="a1c4c-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="a1c4c-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="a1c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c4c-103">가상 머신, 네트워크 어댑터 또는 PaaS 역할에 대 한 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="a1c4c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1c4c-104">SYNTAX</span></span>

### <span data-ttu-id="a1c4c-105">Getnetworksecuritygrouationnetworkforsubnet</span><span class="sxs-lookup"><span data-stu-id="a1c4c-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a1c4c-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="a1c4c-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a1c4c-107">Getnetworksecuritygroupayationasrole</span><span class="sxs-lookup"><span data-stu-id="a1c4c-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a1c4c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a1c4c-108">DESCRIPTION</span></span>
<span data-ttu-id="a1c4c-109">**AzureNetworkSecurityGroupAssociation** cmdlet은 가상 머신, 네트워크 어댑터 또는 플랫폼 as 서비스 (PaaS) 역할에 대 한 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="a1c4c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a1c4c-110">EXAMPLES</span></span>

### <span data-ttu-id="a1c4c-111">예제 1: 가상 컴퓨터용 네트워크 보안 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1c4c-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="a1c4c-112">이 명령은 ContosoService 이라는 서비스에 대 한 ContosoVM06 이라는 가상 컴퓨터를 가져오고 현재 cmdlet에 해당 가상 컴퓨터 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="a1c4c-113">현재 cmdlet은 해당 가상 컴퓨터와 연결 된 네트워크 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="a1c4c-114">변수</span><span class="sxs-lookup"><span data-stu-id="a1c4c-114">PARAMETERS</span></span>

### <span data-ttu-id="a1c4c-115">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="a1c4c-115">-Detailed</span></span>
<span data-ttu-id="a1c4c-116">이 cmdlet이 가상 컴퓨터와 연결 된 네트워크 보안 그룹의 세부 정보를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="a1c4c-117">이러한 세부 정보에는 위치 및 규칙이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-117">These details include location and rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c4c-118">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a1c4c-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="a1c4c-119">이 cmdlet이 네트워크 보안 그룹을 가져오는 네트워크 어댑터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c4c-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="a1c4c-120">-Profile</span></span>
<span data-ttu-id="a1c4c-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a1c4c-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1c4c-123">-RoleName</span><span class="sxs-lookup"><span data-stu-id="a1c4c-123">-RoleName</span></span>
<span data-ttu-id="a1c4c-124">이 cmdlet이 네트워크 보안 그룹을 가져오는 PaaS 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c4c-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a1c4c-125">-ServiceName</span></span>
<span data-ttu-id="a1c4c-126">클라우드 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="a1c4c-127">PaaS 역할은이 매개 변수에서 지정 하는 서비스에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c4c-128">-슬롯</span><span class="sxs-lookup"><span data-stu-id="a1c4c-128">-Slot</span></span>
<span data-ttu-id="a1c4c-129">PaaS 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="a1c4c-130">이 cmdlet에서 네트워크 보안 그룹을 가져오는 PaaS 역할에이 매개 변수에서 지정 하는 슬롯이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="a1c4c-131">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-131">Valid values are:</span></span> 

- <span data-ttu-id="a1c4c-132">프로덕션용</span><span class="sxs-lookup"><span data-stu-id="a1c4c-132">Production</span></span>
- <span data-ttu-id="a1c4c-133">대기</span><span class="sxs-lookup"><span data-stu-id="a1c4c-133">Staging</span></span> 

<span data-ttu-id="a1c4c-134">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c4c-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a1c4c-135">-SubnetName</span></span>
<span data-ttu-id="a1c4c-136">이 cmdlet이 네트워크 보안 그룹을 가져오는 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c4c-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a1c4c-137">-VirtualNetworkName</span></span>
<span data-ttu-id="a1c4c-138">이 cmdlet이 네트워크 보안 그룹을 가져오는 서브넷을 포함 하는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c4c-139">-VM</span><span class="sxs-lookup"><span data-stu-id="a1c4c-139">-VM</span></span>
<span data-ttu-id="a1c4c-140">이 cmdlet이 네트워크 보안 그룹을 적용 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c4c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c4c-141">CommonParameters</span></span>
<span data-ttu-id="a1c4c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c4c-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c4c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c4c-144">입력</span><span class="sxs-lookup"><span data-stu-id="a1c4c-144">INPUTS</span></span>

## <span data-ttu-id="a1c4c-145">출력</span><span class="sxs-lookup"><span data-stu-id="a1c4c-145">OUTPUTS</span></span>

### <span data-ttu-id="a1c4c-146">WindowsAzure. ServiceManagement를 INetworkSecurityGroup으로 그룹화 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c4c-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="a1c4c-147">상속자</span><span class="sxs-lookup"><span data-stu-id="a1c4c-147">NOTES</span></span>

## <span data-ttu-id="a1c4c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1c4c-148">RELATED LINKS</span></span>

[<span data-ttu-id="a1c4c-149">제거-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="a1c4c-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="a1c4c-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="a1c4c-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


