---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704072"
---
# <span data-ttu-id="b3a58-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="b3a58-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="b3a58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a58-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a58-103">지정 된 통합 런타임을 사용 하 여 연결 된 서비스의 자격 증명을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3a58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3a58-104">SYNTAX</span></span>

### <span data-ttu-id="b3a58-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3a58-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="b3a58-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b3a58-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="b3a58-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b3a58-107">DESCRIPTION</span></span>
<span data-ttu-id="b3a58-108">지정 된 통합 런타임을 사용 하 여 연결 된 서비스의 자격 증명을 암호화 하 New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="b3a58-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b3a58-109">EXAMPLES</span></span>

### <span data-ttu-id="b3a58-110">예제 1: 연결 된 서비스에서 creadentials 암호화</span><span class="sxs-lookup"><span data-stu-id="b3a58-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="b3a58-111">이 명령은 myIR 이라는 통합 런타임을 사용 하 여 파일 D:\sql.js에서 자격 증명을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="b3a58-112">변수</span><span class="sxs-lookup"><span data-stu-id="b3a58-112">PARAMETERS</span></span>

### <span data-ttu-id="b3a58-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a58-113">-DataFactory</span></span>
<span data-ttu-id="b3a58-114">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a58-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b3a58-115">-DataFactoryName</span></span>
<span data-ttu-id="b3a58-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a58-117">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b3a58-117">-DefinitionFile</span></span>
<span data-ttu-id="b3a58-118">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-118">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a58-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b3a58-119">-Force</span></span>
<span data-ttu-id="b3a58-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-120">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a58-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b3a58-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b3a58-122">통합 런타임 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a58-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a58-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3a58-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a58-125">-확인</span><span class="sxs-lookup"><span data-stu-id="b3a58-125">-Confirm</span></span>
<span data-ttu-id="b3a58-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a58-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a58-127">-WhatIf</span></span>
<span data-ttu-id="b3a58-128">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3a58-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="b3a58-129">입력</span><span class="sxs-lookup"><span data-stu-id="b3a58-129">INPUTS</span></span>

### <span data-ttu-id="b3a58-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b3a58-130">System.String</span></span>
<span data-ttu-id="b3a58-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b3a58-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="b3a58-132">출력</span><span class="sxs-lookup"><span data-stu-id="b3a58-132">OUTPUTS</span></span>

### <span data-ttu-id="b3a58-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b3a58-133">System.String</span></span>


## <span data-ttu-id="b3a58-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b3a58-134">NOTES</span></span>

## <span data-ttu-id="b3a58-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3a58-135">RELATED LINKS</span></span>

