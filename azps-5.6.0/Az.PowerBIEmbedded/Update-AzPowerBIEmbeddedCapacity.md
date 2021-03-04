---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 9559eb6ea0b1df4dbb25524a3a2abadffe6f6c7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997514"
---
# <span data-ttu-id="8b455-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b455-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8b455-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b455-102">SYNOPSIS</span></span>
<span data-ttu-id="8b455-103">PowerBI Embedded Capacity의 인스턴스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="8b455-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b455-104">SYNTAX</span></span>

### <span data-ttu-id="8b455-105">ByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="8b455-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b455-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b455-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b455-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b455-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b455-108">설명</span><span class="sxs-lookup"><span data-stu-id="8b455-108">DESCRIPTION</span></span>
<span data-ttu-id="8b455-109">Update-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI Embedded Capacity 인스턴스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="8b455-110">예제</span><span class="sxs-lookup"><span data-stu-id="8b455-110">EXAMPLES</span></span>

### <span data-ttu-id="8b455-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b455-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="8b455-112">리소스 그룹 테스트 그룹에서 testcapacity라는 용량을 수정하여 태그를 key1:value1 및 key2:value2 및 관리자 및 서비스 주체로 testuser1@contoso.com testuser2@contoso.com 설정합니다. 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="8b455-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="8b455-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b455-113">PARAMETERS</span></span>

### <span data-ttu-id="8b455-114">-Administrator</span><span class="sxs-lookup"><span data-stu-id="8b455-114">-Administrator</span></span>
<span data-ttu-id="8b455-115">용량에서 관리자로 설정할 콤마로 구분된 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="8b455-116">서비스 주체의 경우: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="8b455-116">For service principal: <service principal object id>@<tenant id></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b455-117">-DefaultProfile</span></span>
<span data-ttu-id="8b455-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b455-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b455-119">-InputObject</span></span>
<span data-ttu-id="8b455-120">Piping에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="8b455-120">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8b455-121">-Name</span></span>
<span data-ttu-id="8b455-122">PowerBI 임베디드 용량의 이름</span><span class="sxs-lookup"><span data-stu-id="8b455-122">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b455-123">-PassThru</span></span>
<span data-ttu-id="8b455-124">작업이 성공적으로 완료되면 삭제된 용량 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="8b455-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b455-125">-ResourceGroupName</span></span>
<span data-ttu-id="8b455-126">용량이 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="8b455-126">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b455-127">-ResourceId</span></span>
<span data-ttu-id="8b455-128">PowerBI Embedded Capacity ResourceID.</span><span class="sxs-lookup"><span data-stu-id="8b455-128">PowerBI Embedded Capacity ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="8b455-129">-Sku</span></span>
<span data-ttu-id="8b455-130">용량에 대한 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-130">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b455-131">-Tag</span></span>
<span data-ttu-id="8b455-132">용량에 대한 태그로 설정된 해시 테이블 집합의 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-133">-확인</span><span class="sxs-lookup"><span data-stu-id="8b455-133">-Confirm</span></span>
<span data-ttu-id="8b455-134">사용자에게 작업을 수행할지 여부를 확인하라는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-134">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b455-135">-WhatIf</span></span>
<span data-ttu-id="8b455-136">현재 작업이 실제로 수행하지 않고 수행할 작업을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-136">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b455-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b455-137">CommonParameters</span></span>
<span data-ttu-id="8b455-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b455-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b455-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8b455-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b455-140">입력</span><span class="sxs-lookup"><span data-stu-id="8b455-140">INPUTS</span></span>

### <span data-ttu-id="8b455-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8b455-141">System.String</span></span>

### <span data-ttu-id="8b455-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b455-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8b455-143">출력</span><span class="sxs-lookup"><span data-stu-id="8b455-143">OUTPUTS</span></span>

### <span data-ttu-id="8b455-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b455-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="8b455-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b455-145">NOTES</span></span>

## <span data-ttu-id="8b455-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b455-146">RELATED LINKS</span></span>

[<span data-ttu-id="8b455-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b455-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="8b455-148">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="8b455-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
