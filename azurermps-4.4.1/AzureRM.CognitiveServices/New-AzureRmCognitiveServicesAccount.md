---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537468"
---
# <span data-ttu-id="be0d9-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="be0d9-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="be0d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="be0d9-103">인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be0d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be0d9-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be0d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="be0d9-105">DESCRIPTION</span></span>
<span data-ttu-id="be0d9-106">**AzureRmCognitiveServicesAccount** cmdlet은 지정 된 형식 및 SKU의 인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="be0d9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="be0d9-107">EXAMPLES</span></span>

### <span data-ttu-id="be0d9-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="be0d9-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="be0d9-109">변수</span><span class="sxs-lookup"><span data-stu-id="be0d9-109">PARAMETERS</span></span>

### <span data-ttu-id="be0d9-110">-Force</span><span class="sxs-lookup"><span data-stu-id="be0d9-110">-Force</span></span>
<span data-ttu-id="be0d9-111">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be0d9-112">-위치</span><span class="sxs-lookup"><span data-stu-id="be0d9-112">-Location</span></span>
<span data-ttu-id="be0d9-113">계정을 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-113">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be0d9-114">-이름</span><span class="sxs-lookup"><span data-stu-id="be0d9-114">-Name</span></span>
<span data-ttu-id="be0d9-115">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-115">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="be0d9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be0d9-116">-ResourceGroupName</span></span>
<span data-ttu-id="be0d9-117">계정을 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="be0d9-118">리소스 그룹이 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-118">The resource group must already exist.</span></span>

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

### <span data-ttu-id="be0d9-119">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="be0d9-119">-SkuName</span></span>
<span data-ttu-id="be0d9-120">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="be0d9-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be0d9-122">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="be0d9-122">F0 (free tier)</span></span>
- <span data-ttu-id="be0d9-123">S0</span><span class="sxs-lookup"><span data-stu-id="be0d9-123">S0</span></span>
- <span data-ttu-id="be0d9-124">S1</span><span class="sxs-lookup"><span data-stu-id="be0d9-124">S1</span></span>
- <span data-ttu-id="be0d9-125">구성원과</span><span class="sxs-lookup"><span data-stu-id="be0d9-125">S2</span></span>
- <span data-ttu-id="be0d9-126">시스템이</span><span class="sxs-lookup"><span data-stu-id="be0d9-126">S3</span></span>
- <span data-ttu-id="be0d9-127">S4</span><span class="sxs-lookup"><span data-stu-id="be0d9-127">S4</span></span>

<span data-ttu-id="be0d9-128">자세한 내용은 [인식 서비스 api](https://www.microsoft.com/cognitive-services/en-us/apis)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be0d9-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be0d9-129">태그</span><span class="sxs-lookup"><span data-stu-id="be0d9-129">-Tag</span></span>
<span data-ttu-id="be0d9-130">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-130">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be0d9-131">-Type</span><span class="sxs-lookup"><span data-stu-id="be0d9-131">-Type</span></span>
<span data-ttu-id="be0d9-132">만들 계정의 유형을 지정 합니다. 이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be0d9-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="be0d9-133">ComputerVision</span></span>
- <span data-ttu-id="be0d9-134">Emotion</span><span class="sxs-lookup"><span data-stu-id="be0d9-134">Emotion</span></span>
- <span data-ttu-id="be0d9-135">뒷면이</span><span class="sxs-lookup"><span data-stu-id="be0d9-135">Face</span></span>
- <span data-ttu-id="be0d9-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="be0d9-136">LUIS</span></span>
- <span data-ttu-id="be0d9-137">나오는</span><span class="sxs-lookup"><span data-stu-id="be0d9-137">Recommendations</span></span>
- <span data-ttu-id="be0d9-138">연설</span><span class="sxs-lookup"><span data-stu-id="be0d9-138">Speech</span></span>
- <span data-ttu-id="be0d9-139">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="be0d9-139">TextAnalytics</span></span>
- <span data-ttu-id="be0d9-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="be0d9-140">WebLM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be0d9-141">-확인</span><span class="sxs-lookup"><span data-stu-id="be0d9-141">-Confirm</span></span>
<span data-ttu-id="be0d9-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be0d9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be0d9-143">-WhatIf</span></span>
<span data-ttu-id="be0d9-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be0d9-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be0d9-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0d9-146">-DefaultProfile</span></span>
<span data-ttu-id="be0d9-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be0d9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0d9-148">CommonParameters</span></span>
<span data-ttu-id="be0d9-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be0d9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0d9-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be0d9-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0d9-151">입력</span><span class="sxs-lookup"><span data-stu-id="be0d9-151">INPUTS</span></span>

## <span data-ttu-id="be0d9-152">출력</span><span class="sxs-lookup"><span data-stu-id="be0d9-152">OUTPUTS</span></span>

### <span data-ttu-id="be0d9-153">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="be0d9-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="be0d9-154">상속자</span><span class="sxs-lookup"><span data-stu-id="be0d9-154">NOTES</span></span>

## <span data-ttu-id="be0d9-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be0d9-155">RELATED LINKS</span></span>

[<span data-ttu-id="be0d9-156">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="be0d9-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="be0d9-157">제거-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="be0d9-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="be0d9-158">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="be0d9-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
