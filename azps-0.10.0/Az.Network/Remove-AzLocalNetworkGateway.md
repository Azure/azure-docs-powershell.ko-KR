---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 0589fa3f5dd806149c243557b547455af35178b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875326"
---
# <span data-ttu-id="421fd-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="421fd-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="421fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="421fd-102">SYNOPSIS</span></span>
<span data-ttu-id="421fd-103">로컬 네트워크 게이트웨이를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="421fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="421fd-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="421fd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="421fd-105">DESCRIPTION</span></span>
<span data-ttu-id="421fd-106">로컬 네트워크 게이트웨이는 온-프레미스의 VPN 장치를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="421fd-107">**AzLocalNetworkGateway** Cmdlet은 이름 및 리소스 그룹 이름을 기준으로 프레미스 게이트웨이를 나타내는 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="421fd-108">예제의</span><span class="sxs-lookup"><span data-stu-id="421fd-108">EXAMPLES</span></span>

### <span data-ttu-id="421fd-109">1: 로컬 네트워크 게이트웨이 삭제</span><span class="sxs-lookup"><span data-stu-id="421fd-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="421fd-110">리소스 그룹 "myRG" 내에서 이름이 "myLocalGW" 인 로컬 네트워크 게이트웨이의 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="421fd-111">참고: 먼저 **Remove-AzVirtualNetworkGatewayConnection** cmdlet을 사용 하 여 로컬 네트워크 게이트웨이에 대 한 모든 연결을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="421fd-112">변수</span><span class="sxs-lookup"><span data-stu-id="421fd-112">PARAMETERS</span></span>

### <span data-ttu-id="421fd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="421fd-113">-AsJob</span></span>
<span data-ttu-id="421fd-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="421fd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="421fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421fd-115">-DefaultProfile</span></span>
<span data-ttu-id="421fd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="421fd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="421fd-117">-Force</span></span>
<span data-ttu-id="421fd-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="421fd-119">-이름</span><span class="sxs-lookup"><span data-stu-id="421fd-119">-Name</span></span>
<span data-ttu-id="421fd-120">이 cmdlet이 제거 하는 로컬 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="421fd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="421fd-121">-PassThru</span></span>
<span data-ttu-id="421fd-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="421fd-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="421fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="421fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="421fd-125">로컬 네트워크 게이트웨이를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="421fd-126">-확인</span><span class="sxs-lookup"><span data-stu-id="421fd-126">-Confirm</span></span>
<span data-ttu-id="421fd-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="421fd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="421fd-128">-WhatIf</span></span>
<span data-ttu-id="421fd-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="421fd-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="421fd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421fd-131">CommonParameters</span></span>
<span data-ttu-id="421fd-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="421fd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421fd-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="421fd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421fd-134">입력</span><span class="sxs-lookup"><span data-stu-id="421fd-134">INPUTS</span></span>

## <span data-ttu-id="421fd-135">출력</span><span class="sxs-lookup"><span data-stu-id="421fd-135">OUTPUTS</span></span>

## <span data-ttu-id="421fd-136">상속자</span><span class="sxs-lookup"><span data-stu-id="421fd-136">NOTES</span></span>

## <span data-ttu-id="421fd-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="421fd-137">RELATED LINKS</span></span>

[<span data-ttu-id="421fd-138">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="421fd-138">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="421fd-139">새로운 AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="421fd-139">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="421fd-140">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="421fd-140">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)


