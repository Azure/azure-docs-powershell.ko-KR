---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 13ece8d5bb6ec42e59f6a44910d3a3d46dd9d844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528024"
---
# <span data-ttu-id="eebbe-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eebbe-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="eebbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eebbe-102">SYNOPSIS</span></span>
<span data-ttu-id="eebbe-103">부하 분산 장치를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eebbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eebbe-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eebbe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eebbe-105">DESCRIPTION</span></span>
<span data-ttu-id="eebbe-106">**AzureRmLoadBalancer** Cmdlet은 Azure 부하 분산 장치를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="eebbe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eebbe-107">EXAMPLES</span></span>

### <span data-ttu-id="eebbe-108">예제 1: 부하 분산 장치 제거</span><span class="sxs-lookup"><span data-stu-id="eebbe-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="eebbe-109">이 명령은 Myloadbalancer 이라는 리소스 그룹에서 MyLoadBalancer 라는 부하 분산 장치를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="eebbe-110">변수</span><span class="sxs-lookup"><span data-stu-id="eebbe-110">PARAMETERS</span></span>

### <span data-ttu-id="eebbe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eebbe-111">-AsJob</span></span>
<span data-ttu-id="eebbe-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="eebbe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eebbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebbe-113">-DefaultProfile</span></span>
<span data-ttu-id="eebbe-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eebbe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eebbe-115">-Force</span></span>
<span data-ttu-id="eebbe-116">리소스가 할당 되었는지 여부에 관계 없이이 cmdlet이 부하 분산을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eebbe-117">-이름</span><span class="sxs-lookup"><span data-stu-id="eebbe-117">-Name</span></span>
<span data-ttu-id="eebbe-118">제거할 부하 분산 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="eebbe-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eebbe-119">-PassThru</span></span>
<span data-ttu-id="eebbe-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eebbe-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eebbe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eebbe-122">-ResourceGroupName</span></span>
<span data-ttu-id="eebbe-123">제거할 부하 분산 장치를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="eebbe-124">-확인</span><span class="sxs-lookup"><span data-stu-id="eebbe-124">-Confirm</span></span>
<span data-ttu-id="eebbe-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eebbe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eebbe-126">-WhatIf</span></span>
<span data-ttu-id="eebbe-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eebbe-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eebbe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebbe-129">CommonParameters</span></span>
<span data-ttu-id="eebbe-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebbe-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eebbe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebbe-132">입력</span><span class="sxs-lookup"><span data-stu-id="eebbe-132">INPUTS</span></span>

### <span data-ttu-id="eebbe-133">않아야</span><span class="sxs-lookup"><span data-stu-id="eebbe-133">None</span></span>
<span data-ttu-id="eebbe-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eebbe-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eebbe-135">출력</span><span class="sxs-lookup"><span data-stu-id="eebbe-135">OUTPUTS</span></span>

## <span data-ttu-id="eebbe-136">상속자</span><span class="sxs-lookup"><span data-stu-id="eebbe-136">NOTES</span></span>

## <span data-ttu-id="eebbe-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eebbe-137">RELATED LINKS</span></span>

[<span data-ttu-id="eebbe-138">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eebbe-138">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="eebbe-139">새로운 AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eebbe-139">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="eebbe-140">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="eebbe-140">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


