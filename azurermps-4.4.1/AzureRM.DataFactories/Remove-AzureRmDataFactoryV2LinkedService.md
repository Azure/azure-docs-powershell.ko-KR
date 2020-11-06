---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: bba4df58ed4046eeba562e3438119e1d5df40649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531810"
---
# <span data-ttu-id="efaf9-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="efaf9-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="efaf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efaf9-102">SYNOPSIS</span></span>
<span data-ttu-id="efaf9-103">Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efaf9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efaf9-104">SYNTAX</span></span>

### <span data-ttu-id="efaf9-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="efaf9-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efaf9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="efaf9-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efaf9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="efaf9-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efaf9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="efaf9-108">DESCRIPTION</span></span>
<span data-ttu-id="efaf9-109">Remove-AzureRmDataFactoryV2LinkedService cmdlet은 Azure Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="efaf9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="efaf9-110">EXAMPLES</span></span>

### <span data-ttu-id="efaf9-111">예제 1: 연결 된 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="efaf9-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="efaf9-112">이 명령은 WikiADF 이라는 data factory에서 LinkedServiceTest 라는 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="efaf9-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="efaf9-114">변수</span><span class="sxs-lookup"><span data-stu-id="efaf9-114">PARAMETERS</span></span>

### <span data-ttu-id="efaf9-115">-확인</span><span class="sxs-lookup"><span data-stu-id="efaf9-115">-Confirm</span></span>
<span data-ttu-id="efaf9-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efaf9-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="efaf9-117">-DataFactoryName</span></span>
<span data-ttu-id="efaf9-118">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="efaf9-119">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efaf9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="efaf9-120">-Force</span></span>
<span data-ttu-id="efaf9-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="efaf9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efaf9-122">-InputObject</span></span>
<span data-ttu-id="efaf9-123">제거할 LinkedService 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efaf9-124">-이름</span><span class="sxs-lookup"><span data-stu-id="efaf9-124">-Name</span></span>
<span data-ttu-id="efaf9-125">제거할 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="efaf9-126">연결 된 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efaf9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efaf9-127">-ResourceGroupName</span></span>
<span data-ttu-id="efaf9-128">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="efaf9-129">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efaf9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efaf9-130">-ResourceId</span></span>
<span data-ttu-id="efaf9-131">제거할 연결 된 서비스의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="efaf9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efaf9-132">-WhatIf</span></span>
<span data-ttu-id="efaf9-133">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="efaf9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efaf9-134">-DefaultProfile</span></span>
<span data-ttu-id="efaf9-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efaf9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efaf9-136">CommonParameters</span></span>
<span data-ttu-id="efaf9-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efaf9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efaf9-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efaf9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efaf9-139">입력</span><span class="sxs-lookup"><span data-stu-id="efaf9-139">INPUTS</span></span>

### <span data-ttu-id="efaf9-140">DataFactoryV2. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="efaf9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="efaf9-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="efaf9-141">System.String</span></span>

## <span data-ttu-id="efaf9-142">출력</span><span class="sxs-lookup"><span data-stu-id="efaf9-142">OUTPUTS</span></span>

### <span data-ttu-id="efaf9-143">System. 개체</span><span class="sxs-lookup"><span data-stu-id="efaf9-143">System.Object</span></span>

## <span data-ttu-id="efaf9-144">상속자</span><span class="sxs-lookup"><span data-stu-id="efaf9-144">NOTES</span></span>
<span data-ttu-id="efaf9-145">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="efaf9-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="efaf9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efaf9-146">RELATED LINKS</span></span>

[<span data-ttu-id="efaf9-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="efaf9-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="efaf9-148">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="efaf9-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

