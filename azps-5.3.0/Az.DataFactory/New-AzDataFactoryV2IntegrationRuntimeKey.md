---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495631"
---
# <span data-ttu-id="b0b72-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="b0b72-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="b0b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b72-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b72-103">자체 호스팅 통합 런타임 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="b0b72-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0b72-104">SYNTAX</span></span>

### <span data-ttu-id="b0b72-105">ByIntegrationRuntimeName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b0b72-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b72-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b72-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b72-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b0b72-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b72-108">설명</span><span class="sxs-lookup"><span data-stu-id="b0b72-108">DESCRIPTION</span></span>
<span data-ttu-id="b0b72-109">**New-AzDataFactoryV2IntegrationRuntimeKey** cmdlet은 'KeyName' 매개 변수로 지정된 키 이름으로 통합 런타임 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="b0b72-110">이전 키가 잘못되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="b0b72-111">예제</span><span class="sxs-lookup"><span data-stu-id="b0b72-111">EXAMPLES</span></span>

### <span data-ttu-id="b0b72-112">예제 1: 통합 런타임에 대한 새 키 생성</span><span class="sxs-lookup"><span data-stu-id="b0b72-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="b0b72-113">cmdlet은 'test-selfhost-ir'이라는 통합 런타임에 대한 키 'authKey2'를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b0b72-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b72-114">PARAMETERS</span></span>

### <span data-ttu-id="b0b72-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b0b72-115">-DataFactoryName</span></span>
<span data-ttu-id="b0b72-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b72-117">-DefaultProfile</span></span>
<span data-ttu-id="b0b72-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0b72-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b0b72-119">-Force</span></span>
<span data-ttu-id="b0b72-120">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b0b72-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b72-121">-InputObject</span></span>
<span data-ttu-id="b0b72-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b72-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b0b72-123">-KeyName</span></span>
<span data-ttu-id="b0b72-124">자체 호스팅 통합 런타임의 인증 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b72-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b72-125">-Name</span></span>
<span data-ttu-id="b0b72-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b72-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b72-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0b72-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b72-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b72-129">-ResourceId</span></span>
<span data-ttu-id="b0b72-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b72-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0b72-131">-Confirm</span></span>
<span data-ttu-id="b0b72-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b72-133">-WhatIf</span></span>
<span data-ttu-id="b0b72-134">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b0b72-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b72-135">CommonParameters</span></span>
<span data-ttu-id="b0b72-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b72-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b72-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b0b72-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b72-138">입력</span><span class="sxs-lookup"><span data-stu-id="b0b72-138">INPUTS</span></span>

### <span data-ttu-id="b0b72-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b0b72-139">System.String</span></span>

### <span data-ttu-id="b0b72-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b0b72-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b0b72-141">출력</span><span class="sxs-lookup"><span data-stu-id="b0b72-141">OUTPUTS</span></span>

### <span data-ttu-id="b0b72-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="b0b72-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="b0b72-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0b72-143">NOTES</span></span>

## <span data-ttu-id="b0b72-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0b72-144">RELATED LINKS</span></span>

[<span data-ttu-id="b0b72-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="b0b72-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
