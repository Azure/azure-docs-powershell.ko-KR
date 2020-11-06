---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535691"
---
# <span data-ttu-id="add5c-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="add5c-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="add5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="add5c-102">SYNOPSIS</span></span>
<span data-ttu-id="add5c-103">PowerBI 포함 용량의 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="add5c-104">SYNTAX</span></span>

### <span data-ttu-id="add5c-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="add5c-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="add5c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="add5c-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="add5c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="add5c-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="add5c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="add5c-108">DESCRIPTION</span></span>
<span data-ttu-id="add5c-109">Update-AzureRmPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="add5c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="add5c-110">EXAMPLES</span></span>

### <span data-ttu-id="add5c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="add5c-111">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="add5c-112">Resourcegroup으로 태그를 설정 하도록 리소스 그룹 testcapacity에서 testcapacity 라는 용량을 수정 합니다. value1 및 key2: value2 및 관리자가 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="add5c-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="add5c-113">변수</span><span class="sxs-lookup"><span data-stu-id="add5c-113">PARAMETERS</span></span>

### <span data-ttu-id="add5c-114">-관리자</span><span class="sxs-lookup"><span data-stu-id="add5c-114">-Administrator</span></span>
<span data-ttu-id="add5c-115">용량에 관리자로 설정할 쉼표로 구분 된 용량 이름</span><span class="sxs-lookup"><span data-stu-id="add5c-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="add5c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add5c-116">-DefaultProfile</span></span>
<span data-ttu-id="add5c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="add5c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="add5c-118">-InputObject</span></span>
<span data-ttu-id="add5c-119">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="add5c-119">Input object for Piping</span></span>

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

### <span data-ttu-id="add5c-120">-이름</span><span class="sxs-lookup"><span data-stu-id="add5c-120">-Name</span></span>
<span data-ttu-id="add5c-121">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="add5c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="add5c-122">-PassThru</span></span>
<span data-ttu-id="add5c-123">작업이 성공적으로 완료 되 면 삭제 된 용량 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="add5c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add5c-124">-ResourceGroupName</span></span>
<span data-ttu-id="add5c-125">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="add5c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="add5c-126">-ResourceId</span></span>
<span data-ttu-id="add5c-127">PowerBI 포함 용량 ResourceID입니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="add5c-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="add5c-128">-Sku</span></span>
<span data-ttu-id="add5c-129">용량에 대 한 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-129">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="add5c-130">태그</span><span class="sxs-lookup"><span data-stu-id="add5c-130">-Tag</span></span>
<span data-ttu-id="add5c-131">용량에 대 한 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="add5c-132">-확인</span><span class="sxs-lookup"><span data-stu-id="add5c-132">-Confirm</span></span>
<span data-ttu-id="add5c-133">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="add5c-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="add5c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="add5c-134">-WhatIf</span></span>
<span data-ttu-id="add5c-135">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="add5c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add5c-136">CommonParameters</span></span>
<span data-ttu-id="add5c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="add5c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add5c-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add5c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add5c-139">입력</span><span class="sxs-lookup"><span data-stu-id="add5c-139">INPUTS</span></span>

### <span data-ttu-id="add5c-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="add5c-140">System.String</span></span>

### <span data-ttu-id="add5c-141">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="add5c-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="add5c-142">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="add5c-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="add5c-143">출력</span><span class="sxs-lookup"><span data-stu-id="add5c-143">OUTPUTS</span></span>

### <span data-ttu-id="add5c-144">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="add5c-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="add5c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="add5c-145">NOTES</span></span>

## <span data-ttu-id="add5c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="add5c-146">RELATED LINKS</span></span>

[<span data-ttu-id="add5c-147">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="add5c-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="add5c-148">제거-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="add5c-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
