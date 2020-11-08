---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 22e6cf883268520f0568e28041f210268419a9a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217214"
---
# <span data-ttu-id="670ca-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="670ca-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="670ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="670ca-102">SYNOPSIS</span></span>
<span data-ttu-id="670ca-103">PowerBI 포함 용량의 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="670ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="670ca-104">SYNTAX</span></span>

### <span data-ttu-id="670ca-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="670ca-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="670ca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="670ca-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="670ca-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="670ca-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="670ca-108">설명은</span><span class="sxs-lookup"><span data-stu-id="670ca-108">DESCRIPTION</span></span>
<span data-ttu-id="670ca-109">Update-AzPowerBIEmbeddedCapacity cmdlet은 PowerBI 포함 용량의 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="670ca-110">예제의</span><span class="sxs-lookup"><span data-stu-id="670ca-110">EXAMPLES</span></span>

### <span data-ttu-id="670ca-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="670ca-111">Example 1</span></span>
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

<span data-ttu-id="670ca-112">Resourcegroup, key2: value2, 관리자 testuser1@contoso.com , 서비스 사용자로 태그를 설정 하려면 다음을 수행 하 여 리소스 그룹 testcapacity에서 testcapacity 라는 용량을 수정 합니다. testuser2@contoso.com9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="670ca-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="670ca-113">변수</span><span class="sxs-lookup"><span data-stu-id="670ca-113">PARAMETERS</span></span>

### <span data-ttu-id="670ca-114">-관리자</span><span class="sxs-lookup"><span data-stu-id="670ca-114">-Administrator</span></span>
<span data-ttu-id="670ca-115">용량에 관리자로 설정할 쉼표로 구분 된 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="670ca-116">서비스 사용자의 경우: <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="670ca-116">For service principal: <service principal object id>@<tenant id></span></span>

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

### <span data-ttu-id="670ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670ca-117">-DefaultProfile</span></span>
<span data-ttu-id="670ca-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="670ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="670ca-119">-InputObject</span></span>
<span data-ttu-id="670ca-120">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="670ca-120">Input object for Piping</span></span>

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

### <span data-ttu-id="670ca-121">-이름</span><span class="sxs-lookup"><span data-stu-id="670ca-121">-Name</span></span>
<span data-ttu-id="670ca-122">PowerBI 포함 용량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-122">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="670ca-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="670ca-123">-PassThru</span></span>
<span data-ttu-id="670ca-124">작업이 성공적으로 완료 되 면 삭제 된 용량 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="670ca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670ca-125">-ResourceGroupName</span></span>
<span data-ttu-id="670ca-126">용량이 속한 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-126">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="670ca-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="670ca-127">-ResourceId</span></span>
<span data-ttu-id="670ca-128">PowerBI 포함 용량 ResourceID입니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-128">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="670ca-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="670ca-129">-Sku</span></span>
<span data-ttu-id="670ca-130">용량에 대 한 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-130">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="670ca-131">태그</span><span class="sxs-lookup"><span data-stu-id="670ca-131">-Tag</span></span>
<span data-ttu-id="670ca-132">용량에 대 한 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="670ca-133">-확인</span><span class="sxs-lookup"><span data-stu-id="670ca-133">-Confirm</span></span>
<span data-ttu-id="670ca-134">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="670ca-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="670ca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670ca-135">-WhatIf</span></span>
<span data-ttu-id="670ca-136">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="670ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670ca-137">CommonParameters</span></span>
<span data-ttu-id="670ca-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="670ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670ca-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="670ca-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670ca-140">입력</span><span class="sxs-lookup"><span data-stu-id="670ca-140">INPUTS</span></span>

### <span data-ttu-id="670ca-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="670ca-141">System.String</span></span>

### <span data-ttu-id="670ca-142">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="670ca-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="670ca-143">출력</span><span class="sxs-lookup"><span data-stu-id="670ca-143">OUTPUTS</span></span>

### <span data-ttu-id="670ca-144">PSPowerBIEmbeddedCapacity-Azure. \*</span><span class="sxs-lookup"><span data-stu-id="670ca-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="670ca-145">상속자</span><span class="sxs-lookup"><span data-stu-id="670ca-145">NOTES</span></span>

## <span data-ttu-id="670ca-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="670ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="670ca-147">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="670ca-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="670ca-148">제거-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="670ca-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
