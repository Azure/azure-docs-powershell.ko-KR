---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: e93bcc320f14a8311a29c6be9824da16506ea499
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204960"
---
# <span data-ttu-id="b9511-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b9511-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="b9511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9511-102">SYNOPSIS</span></span>
<span data-ttu-id="b9511-103">Azure 가상 WAN을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="b9511-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9511-104">SYNTAX</span></span>

### <span data-ttu-id="b9511-105">ByVirtualWanName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b9511-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9511-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="b9511-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9511-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="b9511-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-VirtualWANType <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9511-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b9511-108">DESCRIPTION</span></span>
<span data-ttu-id="b9511-109">Azure 가상 WAN을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="b9511-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b9511-110">EXAMPLES</span></span>

### <span data-ttu-id="b9511-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9511-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="b9511-112">위의 방법으로 "서쪽 US" 지역에 리소스 그룹 "testRG"을 만들고 Azure의 해당 리소스 그룹에 Azure 가상 WAN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="b9511-113">VirtualWan이 새 속성으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="b9511-114">변수</span><span class="sxs-lookup"><span data-stu-id="b9511-114">PARAMETERS</span></span>

### <span data-ttu-id="b9511-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="b9511-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="b9511-116">VirtualWan에 대 한 분기 트래픽을 분기할 수 있도록 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="b9511-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="b9511-118">VirtualWan에 대 한 vnet에서 vnet로의 트래픽을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9511-119">-AsJob</span></span>
<span data-ttu-id="b9511-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b9511-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9511-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9511-121">-DefaultProfile</span></span>
<span data-ttu-id="b9511-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b9511-123">-Force</span></span>
<span data-ttu-id="b9511-124">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="b9511-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b9511-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9511-125">-InputObject</span></span>
<span data-ttu-id="b9511-126">수정할 가상 wan 개체</span><span class="sxs-lookup"><span data-stu-id="b9511-126">The virtual wan object to be modified</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-127">-이름</span><span class="sxs-lookup"><span data-stu-id="b9511-127">-Name</span></span>
<span data-ttu-id="b9511-128">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-128">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9511-129">-ResourceGroupName</span></span>
<span data-ttu-id="b9511-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9511-131">-ResourceId</span></span>
<span data-ttu-id="b9511-132">가상 wan에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-133">태그</span><span class="sxs-lookup"><span data-stu-id="b9511-133">-Tag</span></span>
<span data-ttu-id="b9511-134">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-135">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="b9511-135">-VirtualWANType</span></span>
<span data-ttu-id="b9511-136">가상 Wan의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-136">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-137">-확인</span><span class="sxs-lookup"><span data-stu-id="b9511-137">-Confirm</span></span>
<span data-ttu-id="b9511-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9511-139">-WhatIf</span></span>
<span data-ttu-id="b9511-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9511-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9511-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9511-142">CommonParameters</span></span>
<span data-ttu-id="b9511-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9511-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9511-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9511-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9511-145">입력</span><span class="sxs-lookup"><span data-stu-id="b9511-145">INPUTS</span></span>

### <span data-ttu-id="b9511-146">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b9511-146">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="b9511-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b9511-147">System.String</span></span>

## <span data-ttu-id="b9511-148">출력</span><span class="sxs-lookup"><span data-stu-id="b9511-148">OUTPUTS</span></span>

### <span data-ttu-id="b9511-149">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b9511-149">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="b9511-150">상속자</span><span class="sxs-lookup"><span data-stu-id="b9511-150">NOTES</span></span>

## <span data-ttu-id="b9511-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9511-151">RELATED LINKS</span></span>

[<span data-ttu-id="b9511-152">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b9511-152">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="b9511-153">새로운 AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b9511-153">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="b9511-154">제거-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="b9511-154">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
