---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 345e7c6365a66abde5f350f20f614d4d6c94b1b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537467"
---
# <span data-ttu-id="e50fc-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e50fc-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="e50fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e50fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e50fc-103">계정 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e50fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e50fc-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e50fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e50fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e50fc-106">**AzureRmCognitiveServicesAccountKey** Cmdlet은 인지 서비스 계정에 대 한 API 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="e50fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e50fc-107">EXAMPLES</span></span>

## <span data-ttu-id="e50fc-108">변수</span><span class="sxs-lookup"><span data-stu-id="e50fc-108">PARAMETERS</span></span>

### <span data-ttu-id="e50fc-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e50fc-109">-Force</span></span>
<span data-ttu-id="e50fc-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e50fc-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e50fc-111">-KeyName</span></span>
<span data-ttu-id="e50fc-112">다시 생성할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-112">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="e50fc-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e50fc-114">Key1</span><span class="sxs-lookup"><span data-stu-id="e50fc-114">Key1</span></span>
- <span data-ttu-id="e50fc-115">Key2</span><span class="sxs-lookup"><span data-stu-id="e50fc-115">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50fc-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e50fc-116">-Name</span></span>
<span data-ttu-id="e50fc-117">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-117">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50fc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e50fc-118">-ResourceGroupName</span></span>
<span data-ttu-id="e50fc-119">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-119">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50fc-120">-확인</span><span class="sxs-lookup"><span data-stu-id="e50fc-120">-Confirm</span></span>
<span data-ttu-id="e50fc-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50fc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50fc-122">-WhatIf</span></span>
<span data-ttu-id="e50fc-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e50fc-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50fc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50fc-125">-DefaultProfile</span></span>
<span data-ttu-id="e50fc-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e50fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50fc-127">CommonParameters</span></span>
<span data-ttu-id="e50fc-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e50fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50fc-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50fc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50fc-130">입력</span><span class="sxs-lookup"><span data-stu-id="e50fc-130">INPUTS</span></span>

## <span data-ttu-id="e50fc-131">출력</span><span class="sxs-lookup"><span data-stu-id="e50fc-131">OUTPUTS</span></span>

### <span data-ttu-id="e50fc-132">CognitiveServices. CognitiveServicesAccountKeys/.</span><span class="sxs-lookup"><span data-stu-id="e50fc-132">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="e50fc-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e50fc-133">NOTES</span></span>

## <span data-ttu-id="e50fc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e50fc-134">RELATED LINKS</span></span>

[<span data-ttu-id="e50fc-135">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e50fc-135">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


