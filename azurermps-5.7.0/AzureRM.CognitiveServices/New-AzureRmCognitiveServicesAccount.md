---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702168"
---
# <span data-ttu-id="1c16d-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1c16d-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="1c16d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c16d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c16d-103">인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c16d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c16d-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c16d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c16d-105">DESCRIPTION</span></span>
<span data-ttu-id="1c16d-106">**AzureRmCognitiveServicesAccount** cmdlet은 지정 된 형식 및 SKU의 인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="1c16d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1c16d-107">EXAMPLES</span></span>

### <span data-ttu-id="1c16d-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="1c16d-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="1c16d-109">변수</span><span class="sxs-lookup"><span data-stu-id="1c16d-109">PARAMETERS</span></span>

### <span data-ttu-id="1c16d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c16d-110">-DefaultProfile</span></span>
<span data-ttu-id="1c16d-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1c16d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c16d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="1c16d-112">-Force</span></span>
<span data-ttu-id="1c16d-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c16d-114">-위치</span><span class="sxs-lookup"><span data-stu-id="1c16d-114">-Location</span></span>
<span data-ttu-id="1c16d-115">계정을 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c16d-116">-이름</span><span class="sxs-lookup"><span data-stu-id="1c16d-116">-Name</span></span>
<span data-ttu-id="1c16d-117">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-117">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="1c16d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c16d-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c16d-119">계정을 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="1c16d-120">리소스 그룹이 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="1c16d-121">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="1c16d-121">-SkuName</span></span>
<span data-ttu-id="1c16d-122">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="1c16d-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c16d-124">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="1c16d-124">F0 (free tier)</span></span>
- <span data-ttu-id="1c16d-125">S0</span><span class="sxs-lookup"><span data-stu-id="1c16d-125">S0</span></span>
- <span data-ttu-id="1c16d-126">S1</span><span class="sxs-lookup"><span data-stu-id="1c16d-126">S1</span></span>
- <span data-ttu-id="1c16d-127">구성원과</span><span class="sxs-lookup"><span data-stu-id="1c16d-127">S2</span></span>
- <span data-ttu-id="1c16d-128">시스템이</span><span class="sxs-lookup"><span data-stu-id="1c16d-128">S3</span></span>
- <span data-ttu-id="1c16d-129">S4</span><span class="sxs-lookup"><span data-stu-id="1c16d-129">S4</span></span>

<span data-ttu-id="1c16d-130">자세한 내용은 [인식 서비스 api](https://www.microsoft.com/cognitive-services/en-us/apis)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1c16d-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c16d-131">태그</span><span class="sxs-lookup"><span data-stu-id="1c16d-131">-Tag</span></span>
<span data-ttu-id="1c16d-132">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c16d-133">-Type</span><span class="sxs-lookup"><span data-stu-id="1c16d-133">-Type</span></span>
<span data-ttu-id="1c16d-134">만들 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-134">Specifies the type of account to create.</span></span> <span data-ttu-id="1c16d-135">이 매개 변수에 허용 되는 현재 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c16d-136">V7 Autosuggest.</span><span class="sxs-lookup"><span data-stu-id="1c16d-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="1c16d-137">Bing 검색</span><span class="sxs-lookup"><span data-stu-id="1c16d-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="1c16d-138">V7를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-138">Bing.Search.v7</span></span>
- <span data-ttu-id="1c16d-139">Bing. 음성</span><span class="sxs-lookup"><span data-stu-id="1c16d-139">Bing.Speech</span></span>
- <span data-ttu-id="1c16d-140">V7 맞춤법 검사.</span><span class="sxs-lookup"><span data-stu-id="1c16d-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="1c16d-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="1c16d-141">ComputerVision</span></span>
- <span data-ttu-id="1c16d-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="1c16d-142">ContentModerator</span></span>
- <span data-ttu-id="1c16d-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="1c16d-143">CustomSpeech</span></span>
- <span data-ttu-id="1c16d-144">CustomVision. 예측</span><span class="sxs-lookup"><span data-stu-id="1c16d-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="1c16d-145">CustomVision. 교육</span><span class="sxs-lookup"><span data-stu-id="1c16d-145">CustomVision.Training</span></span>
- <span data-ttu-id="1c16d-146">Emotion</span><span class="sxs-lookup"><span data-stu-id="1c16d-146">Emotion</span></span>
- <span data-ttu-id="1c16d-147">뒷면이</span><span class="sxs-lookup"><span data-stu-id="1c16d-147">Face</span></span>
- <span data-ttu-id="1c16d-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="1c16d-148">LUIS</span></span>
- <span data-ttu-id="1c16d-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="1c16d-149">QnAMaker</span></span>
- <span data-ttu-id="1c16d-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="1c16d-150">SpeakerRecognition</span></span>
- <span data-ttu-id="1c16d-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="1c16d-151">SpeechTranslation</span></span>
- <span data-ttu-id="1c16d-152">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="1c16d-152">TextAnalytics</span></span>
- <span data-ttu-id="1c16d-153">TextTranslation</span><span class="sxs-lookup"><span data-stu-id="1c16d-153">TextTranslation</span></span>
- <span data-ttu-id="1c16d-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="1c16d-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c16d-155">-확인</span><span class="sxs-lookup"><span data-stu-id="1c16d-155">-Confirm</span></span>
<span data-ttu-id="1c16d-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c16d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c16d-157">-WhatIf</span></span>
<span data-ttu-id="1c16d-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c16d-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c16d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c16d-160">CommonParameters</span></span>
<span data-ttu-id="1c16d-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c16d-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c16d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c16d-163">입력</span><span class="sxs-lookup"><span data-stu-id="1c16d-163">INPUTS</span></span>

### <span data-ttu-id="1c16d-164">않아야</span><span class="sxs-lookup"><span data-stu-id="1c16d-164">None</span></span>
<span data-ttu-id="1c16d-165">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c16d-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c16d-166">출력</span><span class="sxs-lookup"><span data-stu-id="1c16d-166">OUTPUTS</span></span>

### <span data-ttu-id="1c16d-167">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="1c16d-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="1c16d-168">상속자</span><span class="sxs-lookup"><span data-stu-id="1c16d-168">NOTES</span></span>

## <span data-ttu-id="1c16d-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c16d-169">RELATED LINKS</span></span>

[<span data-ttu-id="1c16d-170">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1c16d-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="1c16d-171">제거-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1c16d-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="1c16d-172">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1c16d-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
