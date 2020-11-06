---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526992"
---
# <span data-ttu-id="4aaf6-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="4aaf6-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="4aaf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aaf6-102">SYNOPSIS</span></span>
<span data-ttu-id="4aaf6-103">계정 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aaf6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4aaf6-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aaf6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4aaf6-105">DESCRIPTION</span></span>
<span data-ttu-id="4aaf6-106">**AzureRmCognitiveServicesAccountKey** Cmdlet은 인지 서비스 계정에 대 한 API 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="4aaf6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4aaf6-107">EXAMPLES</span></span>

## <span data-ttu-id="4aaf6-108">변수</span><span class="sxs-lookup"><span data-stu-id="4aaf6-108">PARAMETERS</span></span>

### <span data-ttu-id="4aaf6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aaf6-109">-DefaultProfile</span></span>
<span data-ttu-id="4aaf6-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4aaf6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4aaf6-111">-Force</span></span>
<span data-ttu-id="4aaf6-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4aaf6-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4aaf6-113">-KeyName</span></span>
<span data-ttu-id="4aaf6-114">다시 생성할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="4aaf6-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4aaf6-116">Key1</span><span class="sxs-lookup"><span data-stu-id="4aaf6-116">Key1</span></span>
- <span data-ttu-id="4aaf6-117">Key2</span><span class="sxs-lookup"><span data-stu-id="4aaf6-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4aaf6-118">-Name</span></span>
<span data-ttu-id="4aaf6-119">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-119">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aaf6-120">-ResourceGroupName</span></span>
<span data-ttu-id="4aaf6-121">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-121">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-122">-확인</span><span class="sxs-lookup"><span data-stu-id="4aaf6-122">-Confirm</span></span>
<span data-ttu-id="4aaf6-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aaf6-124">-WhatIf</span></span>
<span data-ttu-id="4aaf6-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aaf6-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aaf6-127">CommonParameters</span></span>
<span data-ttu-id="4aaf6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aaf6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aaf6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aaf6-130">입력</span><span class="sxs-lookup"><span data-stu-id="4aaf6-130">INPUTS</span></span>

### <span data-ttu-id="4aaf6-131">않아야</span><span class="sxs-lookup"><span data-stu-id="4aaf6-131">None</span></span>
<span data-ttu-id="4aaf6-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4aaf6-133">출력</span><span class="sxs-lookup"><span data-stu-id="4aaf6-133">OUTPUTS</span></span>

### <span data-ttu-id="4aaf6-134">CognitiveServices. CognitiveServicesAccountKeys/.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="4aaf6-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4aaf6-135">NOTES</span></span>

## <span data-ttu-id="4aaf6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aaf6-136">RELATED LINKS</span></span>

[<span data-ttu-id="4aaf6-137">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="4aaf6-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


