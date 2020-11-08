---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043938"
---
# <span data-ttu-id="2b20b-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b20b-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="2b20b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b20b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b20b-103">기존 VpnServerConfiguration를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="2b20b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b20b-104">SYNTAX</span></span>

### <span data-ttu-id="2b20b-105">ByVpnServerConfigurationName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b20b-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b20b-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2b20b-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b20b-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="2b20b-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b20b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2b20b-108">DESCRIPTION</span></span>
<span data-ttu-id="2b20b-109">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="2b20b-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2b20b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2b20b-110">EXAMPLES</span></span>

### <span data-ttu-id="2b20b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b20b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="2b20b-112">위의 명령은 기존 VpnServerConfiguration를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="2b20b-113">변수</span><span class="sxs-lookup"><span data-stu-id="2b20b-113">PARAMETERS</span></span>

### <span data-ttu-id="2b20b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b20b-114">-DefaultProfile</span></span>
<span data-ttu-id="2b20b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b20b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2b20b-116">-Force</span></span>
<span data-ttu-id="2b20b-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2b20b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b20b-118">-InputObject</span></span>
<span data-ttu-id="2b20b-119">삭제할 vpnServerConfiguration 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="2b20b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2b20b-120">-Name</span></span>
<span data-ttu-id="2b20b-121">VpnServerConfiguration 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="2b20b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b20b-122">-PassThru</span></span>
<span data-ttu-id="2b20b-123">이 작업이 수행 되는 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="2b20b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b20b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b20b-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-125">The resource group name.</span></span>

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

### <span data-ttu-id="2b20b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b20b-126">-ResourceId</span></span>
<span data-ttu-id="2b20b-127">삭제할 vpnServerConfiguration의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="2b20b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="2b20b-128">-Confirm</span></span>
<span data-ttu-id="2b20b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b20b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b20b-130">-WhatIf</span></span>
<span data-ttu-id="2b20b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b20b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b20b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b20b-133">CommonParameters</span></span>
<span data-ttu-id="2b20b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b20b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b20b-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b20b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b20b-136">입력</span><span class="sxs-lookup"><span data-stu-id="2b20b-136">INPUTS</span></span>

### <span data-ttu-id="2b20b-137">PSVpnServerConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2b20b-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="2b20b-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2b20b-138">System.String</span></span>

## <span data-ttu-id="2b20b-139">출력</span><span class="sxs-lookup"><span data-stu-id="2b20b-139">OUTPUTS</span></span>

### <span data-ttu-id="2b20b-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2b20b-140">System.Boolean</span></span>

## <span data-ttu-id="2b20b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="2b20b-141">NOTES</span></span>

## <span data-ttu-id="2b20b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b20b-142">RELATED LINKS</span></span>
