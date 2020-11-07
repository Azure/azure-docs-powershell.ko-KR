---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: ddd1ab1ce748def345604447988d0fc53b5989fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704170"
---
# <span data-ttu-id="dff22-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="dff22-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="dff22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dff22-102">SYNOPSIS</span></span>
<span data-ttu-id="dff22-103">경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dff22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dff22-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dff22-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dff22-105">DESCRIPTION</span></span>
<span data-ttu-id="dff22-106">**AzureRmRouteTable** Cmdlet은 Azure 경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="dff22-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dff22-107">EXAMPLES</span></span>

### <span data-ttu-id="dff22-108">예제 1: 경로 테이블 제거</span><span class="sxs-lookup"><span data-stu-id="dff22-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="dff22-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 RouteTable01 이라는 경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="dff22-110">테이블을 제거 하기 전에 확인 하 라는 메시지가 cmdlet에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="dff22-111">변수</span><span class="sxs-lookup"><span data-stu-id="dff22-111">PARAMETERS</span></span>

### <span data-ttu-id="dff22-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dff22-112">-AsJob</span></span>
<span data-ttu-id="dff22-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dff22-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dff22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff22-114">-DefaultProfile</span></span>
<span data-ttu-id="dff22-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dff22-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dff22-116">-Force</span></span>
<span data-ttu-id="dff22-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dff22-118">-이름</span><span class="sxs-lookup"><span data-stu-id="dff22-118">-Name</span></span>
<span data-ttu-id="dff22-119">이 cmdlet이 제거 하는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dff22-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dff22-120">-PassThru</span></span>
<span data-ttu-id="dff22-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dff22-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dff22-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff22-123">-ResourceGroupName</span></span>
<span data-ttu-id="dff22-124">이 cmdlet이 제거 하는 경로 테이블이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dff22-125">-확인</span><span class="sxs-lookup"><span data-stu-id="dff22-125">-Confirm</span></span>
<span data-ttu-id="dff22-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff22-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff22-127">-WhatIf</span></span>
<span data-ttu-id="dff22-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff22-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff22-130">CommonParameters</span></span>
<span data-ttu-id="dff22-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff22-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff22-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff22-133">입력</span><span class="sxs-lookup"><span data-stu-id="dff22-133">INPUTS</span></span>

### <span data-ttu-id="dff22-134">않아야</span><span class="sxs-lookup"><span data-stu-id="dff22-134">None</span></span>
<span data-ttu-id="dff22-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dff22-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dff22-136">출력</span><span class="sxs-lookup"><span data-stu-id="dff22-136">OUTPUTS</span></span>

## <span data-ttu-id="dff22-137">상속자</span><span class="sxs-lookup"><span data-stu-id="dff22-137">NOTES</span></span>

## <span data-ttu-id="dff22-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dff22-138">RELATED LINKS</span></span>

[<span data-ttu-id="dff22-139">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="dff22-139">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="dff22-140">새로운 AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="dff22-140">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="dff22-141">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="dff22-141">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


