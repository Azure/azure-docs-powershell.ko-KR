---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: a3bccd635c5bb2a91cb0b8ea9bc09f93070d447d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528547"
---
# <span data-ttu-id="d52a6-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d52a6-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="d52a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d52a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d52a6-103">자체 호스팅 통합 런타임 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d52a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d52a6-104">SYNTAX</span></span>

### <span data-ttu-id="d52a6-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d52a6-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d52a6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d52a6-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d52a6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d52a6-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d52a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d52a6-108">DESCRIPTION</span></span>
<span data-ttu-id="d52a6-109">Cmdlet **AzureRmDataFactoryV2IntegrationRuntimeKey** 는 ' KeyName ' 매개 변수에 의해 지정 된 키 이름을 사용 하 여 통합 런타임 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="d52a6-110">이전 키가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="d52a6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d52a6-111">EXAMPLES</span></span>

### <span data-ttu-id="d52a6-112">예제 1: 통합 런타임에 대 한 새 키 생성</span><span class="sxs-lookup"><span data-stu-id="d52a6-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="d52a6-113">Cmdlet은 ' test-selfhost-ir ' 이라는 통합 런타임에 대 한 ' authKey2 ' 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="d52a6-114">변수</span><span class="sxs-lookup"><span data-stu-id="d52a6-114">PARAMETERS</span></span>

### <span data-ttu-id="d52a6-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d52a6-115">-DataFactoryName</span></span>
<span data-ttu-id="d52a6-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-116">The data factory name.</span></span>

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

### <span data-ttu-id="d52a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52a6-117">-DefaultProfile</span></span>
<span data-ttu-id="d52a6-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d52a6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d52a6-119">-Force</span></span>
<span data-ttu-id="d52a6-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d52a6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d52a6-121">-InputObject</span></span>
<span data-ttu-id="d52a6-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="d52a6-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d52a6-123">-KeyName</span></span>
<span data-ttu-id="d52a6-124">자체 호스팅 통합 런타임의 인증 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="d52a6-125">-이름</span><span class="sxs-lookup"><span data-stu-id="d52a6-125">-Name</span></span>
<span data-ttu-id="d52a6-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="d52a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d52a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d52a6-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-128">The resource group name.</span></span>

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

### <span data-ttu-id="d52a6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d52a6-129">-ResourceId</span></span>
<span data-ttu-id="d52a6-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d52a6-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d52a6-131">-Confirm</span></span>
<span data-ttu-id="d52a6-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d52a6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d52a6-133">-WhatIf</span></span>
<span data-ttu-id="d52a6-134">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d52a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52a6-135">CommonParameters</span></span>
<span data-ttu-id="d52a6-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d52a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52a6-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d52a6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52a6-138">입력</span><span class="sxs-lookup"><span data-stu-id="d52a6-138">INPUTS</span></span>

### <span data-ttu-id="d52a6-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d52a6-139">System.String</span></span>

### <span data-ttu-id="d52a6-140">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="d52a6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="d52a6-141">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d52a6-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d52a6-142">출력</span><span class="sxs-lookup"><span data-stu-id="d52a6-142">OUTPUTS</span></span>

### <span data-ttu-id="d52a6-143">DataFactoryV2. PSIntegrationRuntimeKeys/.</span><span class="sxs-lookup"><span data-stu-id="d52a6-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="d52a6-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d52a6-144">NOTES</span></span>

## <span data-ttu-id="d52a6-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d52a6-145">RELATED LINKS</span></span>

[<span data-ttu-id="d52a6-146">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d52a6-146">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
