---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208720"
---
# <span data-ttu-id="10273-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="10273-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="10273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10273-102">SYNOPSIS</span></span>
<span data-ttu-id="10273-103">지정된 통합 런타임으로 연결된 서비스의 자격 증명을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="10273-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="10273-104">구문</span><span class="sxs-lookup"><span data-stu-id="10273-104">SYNTAX</span></span>

### <span data-ttu-id="10273-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="10273-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10273-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="10273-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10273-107">설명</span><span class="sxs-lookup"><span data-stu-id="10273-107">DESCRIPTION</span></span>
<span data-ttu-id="10273-108">이 New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet은 지정된 통합 런타임으로 연결된 서비스의 자격 증명을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="10273-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="10273-109">다음 전제가 충족되도록 하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="10273-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="10273-110">**원격 액세스** 옵션은 자체 호스팅 통합 런타임에서 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="10273-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="10273-111">Powershell 7.0 이상은 cmdlet을 실행하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="10273-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="10273-112">예제</span><span class="sxs-lookup"><span data-stu-id="10273-112">EXAMPLES</span></span>

### <span data-ttu-id="10273-113">예제 1: 연결된 서비스에서 자격 증명 암호화</span><span class="sxs-lookup"><span data-stu-id="10273-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="10273-114">이 명령은 test-selfhost-ir이라는 C:\samples\WikiSample\TaxiDemo1.js런타임에 있는 파일에서 자격 증명을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="10273-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="10273-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10273-115">PARAMETERS</span></span>

### <span data-ttu-id="10273-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="10273-116">-DataFactory</span></span>
<span data-ttu-id="10273-117">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="10273-117">The data factory object.</span></span>

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

### <span data-ttu-id="10273-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="10273-118">-DataFactoryName</span></span>
<span data-ttu-id="10273-119">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10273-119">The data factory name.</span></span>

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

### <span data-ttu-id="10273-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10273-120">-DefaultProfile</span></span>
<span data-ttu-id="10273-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10273-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10273-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="10273-122">-DefinitionFile</span></span>
<span data-ttu-id="10273-123">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="10273-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10273-124">-Force</span><span class="sxs-lookup"><span data-stu-id="10273-124">-Force</span></span>
<span data-ttu-id="10273-125">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="10273-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="10273-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="10273-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="10273-127">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10273-127">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10273-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10273-128">-ResourceGroupName</span></span>
<span data-ttu-id="10273-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10273-129">The resource group name.</span></span>

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

### <span data-ttu-id="10273-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10273-130">-Confirm</span></span>
<span data-ttu-id="10273-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10273-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10273-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10273-132">-WhatIf</span></span>
<span data-ttu-id="10273-133">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="10273-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="10273-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10273-134">CommonParameters</span></span>
<span data-ttu-id="10273-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10273-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10273-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="10273-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10273-137">입력</span><span class="sxs-lookup"><span data-stu-id="10273-137">INPUTS</span></span>

### <span data-ttu-id="10273-138">System.String</span><span class="sxs-lookup"><span data-stu-id="10273-138">System.String</span></span>

### <span data-ttu-id="10273-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="10273-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="10273-140">출력</span><span class="sxs-lookup"><span data-stu-id="10273-140">OUTPUTS</span></span>

### <span data-ttu-id="10273-141">System.String</span><span class="sxs-lookup"><span data-stu-id="10273-141">System.String</span></span>

## <span data-ttu-id="10273-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10273-142">NOTES</span></span>

## <span data-ttu-id="10273-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10273-143">RELATED LINKS</span></span>
