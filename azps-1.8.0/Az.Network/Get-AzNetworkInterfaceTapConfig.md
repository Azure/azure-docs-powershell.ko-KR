---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: d8e9eda6c6507974376dc35e80a30669bd940153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700541"
---
# <span data-ttu-id="a70a4-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a70a4-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="a70a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a70a4-102">SYNOPSIS</span></span>
<span data-ttu-id="a70a4-103">탭 구성 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="a70a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a70a4-104">SYNTAX</span></span>

### <span data-ttu-id="a70a4-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a70a4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a70a4-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a70a4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70a4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a70a4-107">DESCRIPTION</span></span>
<span data-ttu-id="a70a4-108">**AzNetworkInterfaceTapConfig** cmdlet은 지정 된 리소스 그룹, 네트워크 인터페이스에 대 한 Azure 탭 구성을 가져오고 리소스 그룹 및 네트워크 인터페이스에서 구성 이름 또는 탭 구성 목록을 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="a70a4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a70a4-109">EXAMPLES</span></span>

### <span data-ttu-id="a70a4-110">예제 1: 지정 된 네트워크 인터페이스에 대 한 모든 탭 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="a70a4-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="a70a4-111">이 명령은 지정 된 네트워크 인터페이스에 추가 된 구성을 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="a70a4-112">예제 2: 지정 된 탭 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="a70a4-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="a70a4-113">이 명령은 주어진 네트워크 인터페이스에 추가 된 특정 탭 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="a70a4-114">예제 3: 지정 된 탭 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="a70a4-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="a70a4-115">이 명령은 "tapconfig"로 시작 하는 이름을 사용 하 여 지정 된 네트워크 인터페이스에 추가 된 구성을 탭 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="a70a4-116">변수</span><span class="sxs-lookup"><span data-stu-id="a70a4-116">PARAMETERS</span></span>

### <span data-ttu-id="a70a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70a4-117">-DefaultProfile</span></span>
<span data-ttu-id="a70a4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70a4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a70a4-119">-Name</span></span>
<span data-ttu-id="a70a4-120">특정 탭 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a70a4-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a70a4-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="a70a4-122">네트워크 인터페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="a70a4-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70a4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a70a4-125">-ResourceId</span></span>
<span data-ttu-id="a70a4-126">TapConfiguration 리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70a4-127">-확인</span><span class="sxs-lookup"><span data-stu-id="a70a4-127">-Confirm</span></span>
<span data-ttu-id="a70a4-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70a4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70a4-129">-WhatIf</span></span>
<span data-ttu-id="a70a4-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a70a4-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70a4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70a4-132">CommonParameters</span></span>
<span data-ttu-id="a70a4-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a70a4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70a4-134">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a70a4-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70a4-135">입력</span><span class="sxs-lookup"><span data-stu-id="a70a4-135">INPUTS</span></span>

### <span data-ttu-id="a70a4-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a70a4-136">System.String</span></span>

## <span data-ttu-id="a70a4-137">출력</span><span class="sxs-lookup"><span data-stu-id="a70a4-137">OUTPUTS</span></span>

### <span data-ttu-id="a70a4-138">PSNetworkInterfaceTapConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a70a4-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="a70a4-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a70a4-139">NOTES</span></span>

## <span data-ttu-id="a70a4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a70a4-140">RELATED LINKS</span></span>

[<span data-ttu-id="a70a4-141">추가-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a70a4-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="a70a4-142">제거-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a70a4-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="a70a4-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a70a4-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
