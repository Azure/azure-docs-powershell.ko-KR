---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: f5451b2c3af331f0086f39f46028aff1d33bf002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990005"
---
# <span data-ttu-id="ad1fb-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad1fb-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="ad1fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad1fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1fb-103">기존 VpnServerConfiguration을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="ad1fb-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad1fb-104">SYNTAX</span></span>

### <span data-ttu-id="ad1fb-105">ByVpnServerConfigurationName(기본값)</span><span class="sxs-lookup"><span data-stu-id="ad1fb-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad1fb-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="ad1fb-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad1fb-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="ad1fb-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad1fb-108">설명</span><span class="sxs-lookup"><span data-stu-id="ad1fb-108">DESCRIPTION</span></span>
<span data-ttu-id="ad1fb-109">{{Description}} 채우기}</span><span class="sxs-lookup"><span data-stu-id="ad1fb-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ad1fb-110">예제</span><span class="sxs-lookup"><span data-stu-id="ad1fb-110">EXAMPLES</span></span>

### <span data-ttu-id="ad1fb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad1fb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="ad1fb-112">위의 명령은 기존 VpnServerConfiguration을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="ad1fb-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ad1fb-113">PARAMETERS</span></span>

### <span data-ttu-id="ad1fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1fb-114">-DefaultProfile</span></span>
<span data-ttu-id="ad1fb-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad1fb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ad1fb-116">-Force</span></span>
<span data-ttu-id="ad1fb-117">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ad1fb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad1fb-118">-InputObject</span></span>
<span data-ttu-id="ad1fb-119">삭제할 vpnServerConfiguration 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1fb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ad1fb-120">-Name</span></span>
<span data-ttu-id="ad1fb-121">vpnServerConfiguration 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1fb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad1fb-122">-PassThru</span></span>
<span data-ttu-id="ad1fb-123">이 작업이 수행되는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ad1fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad1fb-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1fb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad1fb-126">-ResourceId</span></span>
<span data-ttu-id="ad1fb-127">삭제할 vpnServerConfiguration에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1fb-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ad1fb-128">-Confirm</span></span>
<span data-ttu-id="ad1fb-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad1fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad1fb-130">-WhatIf</span></span>
<span data-ttu-id="ad1fb-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad1fb-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad1fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1fb-133">CommonParameters</span></span>
<span data-ttu-id="ad1fb-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1fb-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ad1fb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1fb-136">입력</span><span class="sxs-lookup"><span data-stu-id="ad1fb-136">INPUTS</span></span>

### <span data-ttu-id="ad1fb-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad1fb-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="ad1fb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ad1fb-138">System.String</span></span>

## <span data-ttu-id="ad1fb-139">출력</span><span class="sxs-lookup"><span data-stu-id="ad1fb-139">OUTPUTS</span></span>

### <span data-ttu-id="ad1fb-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad1fb-140">System.Boolean</span></span>

## <span data-ttu-id="ad1fb-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ad1fb-141">NOTES</span></span>

## <span data-ttu-id="ad1fb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad1fb-142">RELATED LINKS</span></span>
