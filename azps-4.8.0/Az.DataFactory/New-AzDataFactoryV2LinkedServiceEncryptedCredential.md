---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 0ff9ef1337a1f2a5f0503c59dc4e6240d3c959b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047880"
---
# <span data-ttu-id="f996c-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="f996c-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="f996c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f996c-102">SYNOPSIS</span></span>
<span data-ttu-id="f996c-103">지정 된 통합 런타임을 사용 하 여 연결 된 서비스의 자격 증명을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="f996c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f996c-104">SYNTAX</span></span>

### <span data-ttu-id="f996c-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f996c-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f996c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f996c-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f996c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f996c-107">DESCRIPTION</span></span>
<span data-ttu-id="f996c-108">지정 된 통합 런타임을 사용 하 여 연결 된 서비스의 자격 증명을 암호화 하 New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="f996c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f996c-109">EXAMPLES</span></span>

### <span data-ttu-id="f996c-110">예제 1: 연결 된 서비스의 자격 증명 암호화</span><span class="sxs-lookup"><span data-stu-id="f996c-110">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="f996c-111">이 명령은 selfhost-ir 이라는 통합 런타임을 사용 하 여 파일 C:\samples\WikiSample\TaxiDemo1.js에서 자격 증명을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-111">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="f996c-112">변수</span><span class="sxs-lookup"><span data-stu-id="f996c-112">PARAMETERS</span></span>

### <span data-ttu-id="f996c-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f996c-113">-DataFactory</span></span>
<span data-ttu-id="f996c-114">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-114">The data factory object.</span></span>

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

### <span data-ttu-id="f996c-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f996c-115">-DataFactoryName</span></span>
<span data-ttu-id="f996c-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-116">The data factory name.</span></span>

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

### <span data-ttu-id="f996c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f996c-117">-DefaultProfile</span></span>
<span data-ttu-id="f996c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f996c-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f996c-119">-DefinitionFile</span></span>
<span data-ttu-id="f996c-120">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-120">The JSON file path.</span></span>

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

### <span data-ttu-id="f996c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f996c-121">-Force</span></span>
<span data-ttu-id="f996c-122">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f996c-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f996c-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="f996c-124">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="f996c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f996c-125">-ResourceGroupName</span></span>
<span data-ttu-id="f996c-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-126">The resource group name.</span></span>

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

### <span data-ttu-id="f996c-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f996c-127">-Confirm</span></span>
<span data-ttu-id="f996c-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f996c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f996c-129">-WhatIf</span></span>
<span data-ttu-id="f996c-130">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f996c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f996c-131">CommonParameters</span></span>
<span data-ttu-id="f996c-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f996c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f996c-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f996c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f996c-134">입력</span><span class="sxs-lookup"><span data-stu-id="f996c-134">INPUTS</span></span>

### <span data-ttu-id="f996c-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f996c-135">System.String</span></span>

### <span data-ttu-id="f996c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f996c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f996c-137">출력</span><span class="sxs-lookup"><span data-stu-id="f996c-137">OUTPUTS</span></span>

### <span data-ttu-id="f996c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f996c-138">System.String</span></span>

## <span data-ttu-id="f996c-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f996c-139">NOTES</span></span>

## <span data-ttu-id="f996c-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f996c-140">RELATED LINKS</span></span>
