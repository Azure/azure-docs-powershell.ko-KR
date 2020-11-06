---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
ms.openlocfilehash: 1a6c5ae69ef6aa6dc0f64d118fcbc733c97e23a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529480"
---
# <span data-ttu-id="8df07-101">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8df07-101">Remove-AzureRmFirewall</span></span>

## <span data-ttu-id="8df07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8df07-102">SYNOPSIS</span></span>
<span data-ttu-id="8df07-103">방화벽을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-103">Remove a Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8df07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8df07-104">SYNTAX</span></span>

```
Remove-AzureRmFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df07-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8df07-105">DESCRIPTION</span></span>
<span data-ttu-id="8df07-106">**AzureRmFirewall** Cmdlet은 Azure 방화벽을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-106">The **Remove-AzureRmFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="8df07-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8df07-107">EXAMPLES</span></span>

### <span data-ttu-id="8df07-108">1: 방화벽 만들기 및 삭제</span><span class="sxs-lookup"><span data-stu-id="8df07-108">1: Create and delete a Firewall</span></span>
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="8df07-109">이 예제에서는 방화벽을 만든 다음 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="8df07-110">방화벽을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="8df07-111">2: 방화벽을 할당 취소 한 다음 방화벽을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzureRmFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="8df07-112">이 예제에서는 방화벽을 검색 하 고 방화벽을 할당 해제 한 다음 방화벽을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="8df07-113">할당 취소 명령은 실행 중인 서비스를 제거 하지만 방화벽 구성을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="8df07-114">사용자가 서비스를 다시 시작 하려고 하면 방화벽에서 Allocate 메서드를 호출 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="8df07-115">방화벽을 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="8df07-116">변수</span><span class="sxs-lookup"><span data-stu-id="8df07-116">PARAMETERS</span></span>

### <span data-ttu-id="8df07-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8df07-117">-AsJob</span></span>
<span data-ttu-id="8df07-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8df07-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8df07-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df07-119">-DefaultProfile</span></span>
<span data-ttu-id="8df07-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8df07-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8df07-121">-Force</span></span>
<span data-ttu-id="8df07-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8df07-123">-이름</span><span class="sxs-lookup"><span data-stu-id="8df07-123">-Name</span></span>
<span data-ttu-id="8df07-124">이 cmdlet이 제거 하는 방화벽의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8df07-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8df07-125">-PassThru</span></span>
<span data-ttu-id="8df07-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8df07-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8df07-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df07-128">-ResourceGroupName</span></span>
<span data-ttu-id="8df07-129">이 cmdlet이 제거 하는 방화벽을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8df07-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8df07-130">-Confirm</span></span>
<span data-ttu-id="8df07-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8df07-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df07-132">-WhatIf</span></span>
<span data-ttu-id="8df07-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8df07-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8df07-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df07-135">CommonParameters</span></span>
<span data-ttu-id="8df07-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df07-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8df07-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df07-138">입력</span><span class="sxs-lookup"><span data-stu-id="8df07-138">INPUTS</span></span>

### <span data-ttu-id="8df07-139">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="8df07-139">PSAzureFirewall</span></span>
<span data-ttu-id="8df07-140">파이프라인에서 ' PSAzureFirewall ' 유형을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8df07-140">Type 'PSAzureFirewall' is accepted from the pipeline</span></span>

## <span data-ttu-id="8df07-141">출력</span><span class="sxs-lookup"><span data-stu-id="8df07-141">OUTPUTS</span></span>

## <span data-ttu-id="8df07-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8df07-142">NOTES</span></span>

## <span data-ttu-id="8df07-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8df07-143">RELATED LINKS</span></span>

[<span data-ttu-id="8df07-144">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8df07-144">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="8df07-145">새로운 AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8df07-145">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="8df07-146">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8df07-146">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
