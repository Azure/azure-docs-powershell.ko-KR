---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216883"
---
# <span data-ttu-id="8c97a-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c97a-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="8c97a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c97a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c97a-103">경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-103">Removes a route table.</span></span>

## <span data-ttu-id="8c97a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8c97a-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c97a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8c97a-105">DESCRIPTION</span></span>
<span data-ttu-id="8c97a-106">**AzRouteTable** Cmdlet은 Azure 경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="8c97a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8c97a-107">EXAMPLES</span></span>

### <span data-ttu-id="8c97a-108">예제 1: 경로 테이블 제거</span><span class="sxs-lookup"><span data-stu-id="8c97a-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="8c97a-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 RouteTable01 이라는 경로 테이블을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="8c97a-110">테이블을 제거 하기 전에 확인 하 라는 메시지가 cmdlet에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="8c97a-111">변수</span><span class="sxs-lookup"><span data-stu-id="8c97a-111">PARAMETERS</span></span>

### <span data-ttu-id="8c97a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c97a-112">-AsJob</span></span>
<span data-ttu-id="8c97a-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8c97a-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c97a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c97a-114">-DefaultProfile</span></span>
<span data-ttu-id="8c97a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c97a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8c97a-116">-Force</span></span>
<span data-ttu-id="8c97a-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c97a-118">-이름</span><span class="sxs-lookup"><span data-stu-id="8c97a-118">-Name</span></span>
<span data-ttu-id="8c97a-119">이 cmdlet이 제거 하는 경로 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c97a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c97a-120">-PassThru</span></span>
<span data-ttu-id="8c97a-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c97a-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c97a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c97a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c97a-124">이 cmdlet이 제거 하는 경로 테이블이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8c97a-125">-확인</span><span class="sxs-lookup"><span data-stu-id="8c97a-125">-Confirm</span></span>
<span data-ttu-id="8c97a-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c97a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c97a-127">-WhatIf</span></span>
<span data-ttu-id="8c97a-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c97a-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c97a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c97a-130">CommonParameters</span></span>
<span data-ttu-id="8c97a-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8c97a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c97a-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c97a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c97a-133">입력</span><span class="sxs-lookup"><span data-stu-id="8c97a-133">INPUTS</span></span>

### <span data-ttu-id="8c97a-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8c97a-134">System.String</span></span>

## <span data-ttu-id="8c97a-135">출력</span><span class="sxs-lookup"><span data-stu-id="8c97a-135">OUTPUTS</span></span>

### <span data-ttu-id="8c97a-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8c97a-136">System.Boolean</span></span>

## <span data-ttu-id="8c97a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8c97a-137">NOTES</span></span>

## <span data-ttu-id="8c97a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c97a-138">RELATED LINKS</span></span>

[<span data-ttu-id="8c97a-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c97a-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="8c97a-140">새로운 AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c97a-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="8c97a-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c97a-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


