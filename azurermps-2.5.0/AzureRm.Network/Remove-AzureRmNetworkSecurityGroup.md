---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 32709a1a0280604b784c9f094478858f8c4bc4ab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880958"
---
# <span data-ttu-id="ddad9-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ddad9-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="ddad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddad9-102">SYNOPSIS</span></span>
<span data-ttu-id="ddad9-103">네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddad9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ddad9-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddad9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ddad9-105">DESCRIPTION</span></span>
<span data-ttu-id="ddad9-106">**AzureRmNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="ddad9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ddad9-107">EXAMPLES</span></span>

### <span data-ttu-id="ddad9-108">예제 1: 네트워크 보안 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="ddad9-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="ddad9-109">이 명령은 TestRG 이라는 리소스 그룹에 있는 NSG-FrontEnd 라는 보안 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="ddad9-110">변수</span><span class="sxs-lookup"><span data-stu-id="ddad9-110">PARAMETERS</span></span>

### <span data-ttu-id="ddad9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddad9-111">-AsJob</span></span>
<span data-ttu-id="ddad9-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ddad9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddad9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddad9-113">-DefaultProfile</span></span>
<span data-ttu-id="ddad9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddad9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ddad9-115">-Force</span></span>
<span data-ttu-id="ddad9-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ddad9-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ddad9-117">-Name</span></span>
<span data-ttu-id="ddad9-118">이 cmdlet이 제거 하는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ddad9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddad9-119">-PassThru</span></span>
<span data-ttu-id="ddad9-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ddad9-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ddad9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddad9-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddad9-123">이 cmdlet이 네트워크 보안 그룹을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="ddad9-124">-확인</span><span class="sxs-lookup"><span data-stu-id="ddad9-124">-Confirm</span></span>
<span data-ttu-id="ddad9-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddad9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddad9-126">-WhatIf</span></span>
<span data-ttu-id="ddad9-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddad9-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddad9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddad9-129">CommonParameters</span></span>
<span data-ttu-id="ddad9-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddad9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddad9-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddad9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddad9-132">입력</span><span class="sxs-lookup"><span data-stu-id="ddad9-132">INPUTS</span></span>

## <span data-ttu-id="ddad9-133">출력</span><span class="sxs-lookup"><span data-stu-id="ddad9-133">OUTPUTS</span></span>

## <span data-ttu-id="ddad9-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ddad9-134">NOTES</span></span>

## <span data-ttu-id="ddad9-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ddad9-135">RELATED LINKS</span></span>

[<span data-ttu-id="ddad9-136">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ddad9-136">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ddad9-137">새로운 AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ddad9-137">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ddad9-138">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ddad9-138">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


