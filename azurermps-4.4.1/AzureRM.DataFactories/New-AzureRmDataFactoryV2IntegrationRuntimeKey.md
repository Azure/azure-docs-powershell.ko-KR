---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: becbcd3e7bbc0a86a2b092921fd5060dd56e927b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711595"
---
# <span data-ttu-id="05eb3-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="05eb3-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="05eb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="05eb3-103">자체 호스팅 통합 런타임 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05eb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05eb3-104">SYNTAX</span></span>

### <span data-ttu-id="05eb3-105">ByIntegrationRuntimeName (기본값)</span><span class="sxs-lookup"><span data-stu-id="05eb3-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05eb3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05eb3-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05eb3-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="05eb3-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05eb3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="05eb3-108">DESCRIPTION</span></span>
<span data-ttu-id="05eb3-109">Cmdlet **AzureRmDataFactoryV2IntegrationRuntimeKey** 는 ' KeyName ' 매개 변수에 의해 지정 된 키 이름을 사용 하 여 통합 런타임 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="05eb3-110">이전 키가 유효 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="05eb3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="05eb3-111">EXAMPLES</span></span>

### <span data-ttu-id="05eb3-112">예제 1: 통합 런타임에 대 한 새 키 생성</span><span class="sxs-lookup"><span data-stu-id="05eb3-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="05eb3-113">Cmdlet은 ' test-selfhost-ir ' 이라는 통합 런타임에 대 한 ' authKey2 ' 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="05eb3-114">변수</span><span class="sxs-lookup"><span data-stu-id="05eb3-114">PARAMETERS</span></span>

### <span data-ttu-id="05eb3-115">-확인</span><span class="sxs-lookup"><span data-stu-id="05eb3-115">-Confirm</span></span>
<span data-ttu-id="05eb3-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05eb3-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="05eb3-117">-DataFactoryName</span></span>
<span data-ttu-id="05eb3-118">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-118">The data factory name.</span></span>

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

### <span data-ttu-id="05eb3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="05eb3-119">-Force</span></span>
<span data-ttu-id="05eb3-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="05eb3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05eb3-121">-InputObject</span></span>
<span data-ttu-id="05eb3-122">통합 런타임 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="05eb3-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="05eb3-123">-KeyName</span></span>
<span data-ttu-id="05eb3-124">자체 호스팅 통합 런타임의 인증 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="05eb3-125">-이름</span><span class="sxs-lookup"><span data-stu-id="05eb3-125">-Name</span></span>
<span data-ttu-id="05eb3-126">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="05eb3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05eb3-127">-ResourceGroupName</span></span>
<span data-ttu-id="05eb3-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-128">The resource group name.</span></span>

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

### <span data-ttu-id="05eb3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05eb3-129">-ResourceId</span></span>
<span data-ttu-id="05eb3-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="05eb3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05eb3-131">-WhatIf</span></span>
<span data-ttu-id="05eb3-132">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="05eb3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05eb3-133">-DefaultProfile</span></span>
<span data-ttu-id="05eb3-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05eb3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05eb3-135">CommonParameters</span></span>
<span data-ttu-id="05eb3-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05eb3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05eb3-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05eb3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05eb3-138">입력</span><span class="sxs-lookup"><span data-stu-id="05eb3-138">INPUTS</span></span>

### <span data-ttu-id="05eb3-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05eb3-139">System.String</span></span>
<span data-ttu-id="05eb3-140">DataFactoryV2. PSIntegrationRuntime/.</span><span class="sxs-lookup"><span data-stu-id="05eb3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="05eb3-141">출력</span><span class="sxs-lookup"><span data-stu-id="05eb3-141">OUTPUTS</span></span>

### <span data-ttu-id="05eb3-142">DataFactoryV2. PSIntegrationRuntimeKeys/.</span><span class="sxs-lookup"><span data-stu-id="05eb3-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="05eb3-143">상속자</span><span class="sxs-lookup"><span data-stu-id="05eb3-143">NOTES</span></span>

## <span data-ttu-id="05eb3-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05eb3-144">RELATED LINKS</span></span>

[<span data-ttu-id="05eb3-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="05eb3-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
