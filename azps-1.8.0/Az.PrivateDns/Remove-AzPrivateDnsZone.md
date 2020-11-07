---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d54dac2689fd751663ebf0046288c4d4ceeae928
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699767"
---
# <span data-ttu-id="72d0a-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="72d0a-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="72d0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="72d0a-103">리소스 그룹에서 개인 DNS 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="72d0a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72d0a-104">SYNTAX</span></span>

### <span data-ttu-id="72d0a-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="72d0a-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d0a-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="72d0a-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72d0a-107">리소스</span><span class="sxs-lookup"><span data-stu-id="72d0a-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72d0a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="72d0a-108">DESCRIPTION</span></span>
<span data-ttu-id="72d0a-109">**AzPrivateDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (사설 도메인 이름 시스템) 영역을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="72d0a-110">영역에 포함 된 모든 레코드 집합도 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="72d0a-111">*PrivateZone* 매개 변수를 사용 하거나 파이프라인 연산자를 사용 하 여 **PrivateDnsZone** 개체를 전달 하거나 *Name* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="72d0a-112">확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="72d0a-113">**PrivateDnsZone** 개체 (파이프라인 또는 *zone* 매개 변수를 통해 전달 됨)를 사용 하 여 영역을 지정 하는 경우에는 로컬 **PrivateDnsZone** 개체가 검색 된 이후 해당 영역이 Azure DNS에서 변경 되지 않습니다 (DNS 영역 리소스에서 직접 작업을 변경 하는 경우에만 해당 영역 내의 레코드 집합에 대 한 작업을 수행 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="72d0a-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="72d0a-114">이는 동시 영역 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="72d0a-115">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="72d0a-116">예제의</span><span class="sxs-lookup"><span data-stu-id="72d0a-116">EXAMPLES</span></span>

### <span data-ttu-id="72d0a-117">예제 1: 개인 영역 제거</span><span class="sxs-lookup"><span data-stu-id="72d0a-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="72d0a-118">이 명령은 MyResourceGroup 이라는 리소스 그룹에서 myzone.com 이라는 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="72d0a-119">변수</span><span class="sxs-lookup"><span data-stu-id="72d0a-119">PARAMETERS</span></span>

### <span data-ttu-id="72d0a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72d0a-120">-DefaultProfile</span></span>
<span data-ttu-id="72d0a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="72d0a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72d0a-122">-이름</span><span class="sxs-lookup"><span data-stu-id="72d0a-122">-Name</span></span>
<span data-ttu-id="72d0a-123">이 cmdlet이 제거 하는 개인 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="72d0a-124">또한 *ResourceGroupName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="72d0a-125">또는 *zone* 매개 변수를 사용 하 여 DNS 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72d0a-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="72d0a-126">-Overwrite</span></span>
<span data-ttu-id="72d0a-127">**PrivateDnsZone** 개체 (파이프라인 또는 *zone* 매개 변수를 통해 전달 됨)를 사용 하 여 영역을 지정 하는 경우에는 로컬 **PrivateDnsZone** 개체가 검색 된 이후 해당 영역이 Azure DNS에서 변경 되지 않습니다 (DNS 영역 리소스에서 직접 작업을 변경 하는 경우에만 해당 영역 내의 레코드 집합에 대 한 작업을 수행 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="72d0a-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="72d0a-128">이는 동시 영역 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="72d0a-129">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72d0a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72d0a-130">-PassThru</span></span>
<span data-ttu-id="72d0a-131">작업의 결과 (부울)를 전달 하는 데 사용 됩니다. 파이프라인에서 개인 영역 삭제</span><span class="sxs-lookup"><span data-stu-id="72d0a-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="72d0a-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="72d0a-132">-PrivateZone</span></span>
<span data-ttu-id="72d0a-133">삭제할 개인 영역 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-133">The private zone object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72d0a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72d0a-134">-ResourceGroupName</span></span>
<span data-ttu-id="72d0a-135">제거할 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="72d0a-136">*ZoneName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="72d0a-137">또는 파이프라인 또는 *zone* 매개 변수를 통해 전달 되는 **PrivateDnsZone** 개체를 사용 하 여 DNS 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72d0a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72d0a-138">-ResourceId</span></span>
<span data-ttu-id="72d0a-139">개인 DNS 영역 ResourceID</span><span class="sxs-lookup"><span data-stu-id="72d0a-139">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72d0a-140">-확인</span><span class="sxs-lookup"><span data-stu-id="72d0a-140">-Confirm</span></span>
<span data-ttu-id="72d0a-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72d0a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72d0a-142">-WhatIf</span></span>
<span data-ttu-id="72d0a-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72d0a-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72d0a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72d0a-145">CommonParameters</span></span>
<span data-ttu-id="72d0a-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72d0a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72d0a-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72d0a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72d0a-148">입력</span><span class="sxs-lookup"><span data-stu-id="72d0a-148">INPUTS</span></span>

### <span data-ttu-id="72d0a-149">PrivateDns. PSPrivateDnsZone/.</span><span class="sxs-lookup"><span data-stu-id="72d0a-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="72d0a-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72d0a-150">System.String</span></span>

## <span data-ttu-id="72d0a-151">출력</span><span class="sxs-lookup"><span data-stu-id="72d0a-151">OUTPUTS</span></span>

### <span data-ttu-id="72d0a-152">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="72d0a-152">System.Boolean</span></span>

## <span data-ttu-id="72d0a-153">상속자</span><span class="sxs-lookup"><span data-stu-id="72d0a-153">NOTES</span></span>

## <span data-ttu-id="72d0a-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72d0a-154">RELATED LINKS</span></span>

[<span data-ttu-id="72d0a-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="72d0a-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="72d0a-156">새로운 AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="72d0a-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="72d0a-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="72d0a-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
