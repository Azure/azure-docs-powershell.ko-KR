---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: a11588c5c8ce4e2a04b3ead13281ab64163bc5ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702310"
---
# <span data-ttu-id="02f48-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="02f48-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="02f48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02f48-102">SYNOPSIS</span></span>
<span data-ttu-id="02f48-103">Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02f48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02f48-104">SYNTAX</span></span>

### <span data-ttu-id="02f48-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="02f48-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02f48-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="02f48-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02f48-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02f48-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f48-108">설명은</span><span class="sxs-lookup"><span data-stu-id="02f48-108">DESCRIPTION</span></span>
<span data-ttu-id="02f48-109">Remove-AzureRmDataFactoryV2LinkedService cmdlet은 Azure Data Factory에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="02f48-110">예제의</span><span class="sxs-lookup"><span data-stu-id="02f48-110">EXAMPLES</span></span>

### <span data-ttu-id="02f48-111">예제 1: 연결 된 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="02f48-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="02f48-112">이 명령은 WikiADF 이라는 data factory에서 LinkedServiceTest 라는 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="02f48-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="02f48-114">변수</span><span class="sxs-lookup"><span data-stu-id="02f48-114">PARAMETERS</span></span>

### <span data-ttu-id="02f48-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="02f48-115">-DataFactoryName</span></span>
<span data-ttu-id="02f48-116">Data factory의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="02f48-117">이 cmdlet은이 매개 변수에서 지정 하는 데이터 팩터리에 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="02f48-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f48-118">-DefaultProfile</span></span>
<span data-ttu-id="02f48-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02f48-120">-Force</span><span class="sxs-lookup"><span data-stu-id="02f48-120">-Force</span></span>
<span data-ttu-id="02f48-121">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="02f48-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02f48-122">-InputObject</span></span>
<span data-ttu-id="02f48-123">제거할 LinkedService 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-123">Specifies the LinkedService object to remove.</span></span>

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

### <span data-ttu-id="02f48-124">-이름</span><span class="sxs-lookup"><span data-stu-id="02f48-124">-Name</span></span>
<span data-ttu-id="02f48-125">제거할 연결 된 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="02f48-126">연결 된 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-126">Name of the linked service.</span></span>

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

### <span data-ttu-id="02f48-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f48-127">-ResourceGroupName</span></span>
<span data-ttu-id="02f48-128">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="02f48-129">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 연결 된 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="02f48-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02f48-130">-ResourceId</span></span>
<span data-ttu-id="02f48-131">제거할 연결 된 서비스의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="02f48-132">-확인</span><span class="sxs-lookup"><span data-stu-id="02f48-132">-Confirm</span></span>
<span data-ttu-id="02f48-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f48-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f48-134">-WhatIf</span></span>
<span data-ttu-id="02f48-135">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="02f48-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f48-136">CommonParameters</span></span>
<span data-ttu-id="02f48-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02f48-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f48-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f48-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f48-139">입력</span><span class="sxs-lookup"><span data-stu-id="02f48-139">INPUTS</span></span>

### <span data-ttu-id="02f48-140">DataFactoryV2. PSLinkedService/.</span><span class="sxs-lookup"><span data-stu-id="02f48-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="02f48-141">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02f48-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="02f48-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02f48-142">System.String</span></span>

## <span data-ttu-id="02f48-143">출력</span><span class="sxs-lookup"><span data-stu-id="02f48-143">OUTPUTS</span></span>

### <span data-ttu-id="02f48-144">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="02f48-144">System.Void</span></span>

## <span data-ttu-id="02f48-145">상속자</span><span class="sxs-lookup"><span data-stu-id="02f48-145">NOTES</span></span>
<span data-ttu-id="02f48-146">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="02f48-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="02f48-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02f48-147">RELATED LINKS</span></span>

[<span data-ttu-id="02f48-148">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="02f48-148">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="02f48-149">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="02f48-149">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

