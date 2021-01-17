---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371617"
---
# <span data-ttu-id="d17af-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d17af-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="d17af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d17af-102">SYNOPSIS</span></span>
<span data-ttu-id="d17af-103">Azure SecurityPartnerProvider를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="d17af-104">구문</span><span class="sxs-lookup"><span data-stu-id="d17af-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d17af-105">설명</span><span class="sxs-lookup"><span data-stu-id="d17af-105">DESCRIPTION</span></span>
<span data-ttu-id="d17af-106">**New-AzSecurityPartnerProvider** cmdlet은 Azure SecurityPartnerProvider를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="d17af-107">예제</span><span class="sxs-lookup"><span data-stu-id="d17af-107">EXAMPLES</span></span>

### <span data-ttu-id="d17af-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d17af-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="d17af-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d17af-109">PARAMETERS</span></span>

### <span data-ttu-id="d17af-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d17af-110">-AsJob</span></span>
<span data-ttu-id="d17af-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d17af-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d17af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17af-112">-DefaultProfile</span></span>
<span data-ttu-id="d17af-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d17af-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d17af-114">-Force</span></span>
<span data-ttu-id="d17af-115">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d17af-116">-Location</span><span class="sxs-lookup"><span data-stu-id="d17af-116">-Location</span></span>
<span data-ttu-id="d17af-117">위치.</span><span class="sxs-lookup"><span data-stu-id="d17af-117">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17af-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d17af-118">-Name</span></span>
<span data-ttu-id="d17af-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17af-120">-ResourceGroupName</span></span>
<span data-ttu-id="d17af-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-121">The resource group name.</span></span>

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

### <span data-ttu-id="d17af-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="d17af-122">-SecurityProviderName</span></span>
<span data-ttu-id="d17af-123">보안 공급자 이름</span><span class="sxs-lookup"><span data-stu-id="d17af-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17af-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="d17af-124">-Tag</span></span>
<span data-ttu-id="d17af-125">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17af-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d17af-126">-VirtualHub</span></span>
<span data-ttu-id="d17af-127">보안 파트너 공급자가 연결된 가상 허브 ID</span><span class="sxs-lookup"><span data-stu-id="d17af-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d17af-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="d17af-128">-VirtualHubId</span></span>
<span data-ttu-id="d17af-129">이 VpnGateway를 연결해야 하는 VirtualHub의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17af-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="d17af-130">-VirtualHubName</span></span>
<span data-ttu-id="d17af-131">이 VpnGateway를 연결해야 하는 VirtualHub의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17af-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d17af-132">-Confirm</span></span>
<span data-ttu-id="d17af-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d17af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d17af-134">-WhatIf</span></span>
<span data-ttu-id="d17af-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d17af-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d17af-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d17af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17af-137">CommonParameters</span></span>
<span data-ttu-id="d17af-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d17af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17af-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d17af-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17af-140">입력</span><span class="sxs-lookup"><span data-stu-id="d17af-140">INPUTS</span></span>

### <span data-ttu-id="d17af-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d17af-141">System.String</span></span>

### <span data-ttu-id="d17af-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d17af-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d17af-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d17af-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d17af-144">출력</span><span class="sxs-lookup"><span data-stu-id="d17af-144">OUTPUTS</span></span>

### <span data-ttu-id="d17af-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d17af-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="d17af-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d17af-146">NOTES</span></span>

## <span data-ttu-id="d17af-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d17af-147">RELATED LINKS</span></span>
