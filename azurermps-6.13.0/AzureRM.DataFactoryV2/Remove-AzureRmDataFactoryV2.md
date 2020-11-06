---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: a4446fb64ed8d279e24b3cf3d6c82701b48ab754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524492"
---
# <span data-ttu-id="34953-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="34953-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="34953-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34953-102">SYNOPSIS</span></span>
<span data-ttu-id="34953-103">Data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34953-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34953-104">SYNTAX</span></span>

### <span data-ttu-id="34953-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="34953-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34953-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="34953-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34953-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="34953-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34953-108">설명은</span><span class="sxs-lookup"><span data-stu-id="34953-108">DESCRIPTION</span></span>
<span data-ttu-id="34953-109">Remove-AzureRmDataFactoryV2 cmdlet은 data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="34953-110">예제의</span><span class="sxs-lookup"><span data-stu-id="34953-110">EXAMPLES</span></span>

### <span data-ttu-id="34953-111">예제 1: data factory 제거</span><span class="sxs-lookup"><span data-stu-id="34953-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="34953-112">이 명령은 ADF 라는 리소스 그룹에서 WikiADF 이라는 data factory를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="34953-113">이 명령은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="34953-114">변수</span><span class="sxs-lookup"><span data-stu-id="34953-114">PARAMETERS</span></span>

### <span data-ttu-id="34953-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34953-115">-DefaultProfile</span></span>
<span data-ttu-id="34953-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34953-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34953-117">-Force</span><span class="sxs-lookup"><span data-stu-id="34953-117">-Force</span></span>
<span data-ttu-id="34953-118">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="34953-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34953-119">-InputObject</span></span>
<span data-ttu-id="34953-120">제거할 DataFactory 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34953-121">-이름</span><span class="sxs-lookup"><span data-stu-id="34953-121">-Name</span></span>
<span data-ttu-id="34953-122">제거할 데이터 팩터리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34953-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34953-123">-ResourceGroupName</span></span>
<span data-ttu-id="34953-124">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="34953-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 데이터 팩터리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34953-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34953-126">-ResourceId</span></span>
<span data-ttu-id="34953-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="34953-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="34953-128">-확인</span><span class="sxs-lookup"><span data-stu-id="34953-128">-Confirm</span></span>
<span data-ttu-id="34953-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34953-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34953-130">-WhatIf</span></span>
<span data-ttu-id="34953-131">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34953-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="34953-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34953-132">CommonParameters</span></span>
<span data-ttu-id="34953-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34953-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34953-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34953-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34953-135">입력</span><span class="sxs-lookup"><span data-stu-id="34953-135">INPUTS</span></span>

### <span data-ttu-id="34953-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="34953-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="34953-137">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="34953-137">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="34953-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34953-138">System.String</span></span>

## <span data-ttu-id="34953-139">출력</span><span class="sxs-lookup"><span data-stu-id="34953-139">OUTPUTS</span></span>

### <span data-ttu-id="34953-140">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="34953-140">System.Void</span></span>

## <span data-ttu-id="34953-141">상속자</span><span class="sxs-lookup"><span data-stu-id="34953-141">NOTES</span></span>
<span data-ttu-id="34953-142">키워드: azure, azurerm, arm, resource, 관리, manager, data, 팩토리</span><span class="sxs-lookup"><span data-stu-id="34953-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="34953-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34953-143">RELATED LINKS</span></span>

[<span data-ttu-id="34953-144">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="34953-144">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="34953-145">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="34953-145">Set-AzureRmDataFactoryV2</span></span>]()
