---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 7e5253951ec3c74850584aaac9818a6a7c8f2737
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701389"
---
# <span data-ttu-id="d5dc2-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d5dc2-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="d5dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="d5dc2-103">인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="d5dc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5dc2-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5dc2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="d5dc2-106">**AzCognitiveServicesAccount** cmdlet은 지정 된 형식 및 SKU의 인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="d5dc2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d5dc2-107">EXAMPLES</span></span>

### <span data-ttu-id="d5dc2-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="d5dc2-108">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="d5dc2-109">변수</span><span class="sxs-lookup"><span data-stu-id="d5dc2-109">PARAMETERS</span></span>

### <span data-ttu-id="d5dc2-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="d5dc2-110">-CustomSubdomainName</span></span>
<span data-ttu-id="d5dc2-111">인지 서비스 계정 하위 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-111">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5dc2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5dc2-112">-DefaultProfile</span></span>
<span data-ttu-id="d5dc2-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d5dc2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5dc2-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d5dc2-114">-Force</span></span>
<span data-ttu-id="d5dc2-115">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d5dc2-116">-위치</span><span class="sxs-lookup"><span data-stu-id="d5dc2-116">-Location</span></span>
<span data-ttu-id="d5dc2-117">계정을 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="d5dc2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d5dc2-118">-Name</span></span>
<span data-ttu-id="d5dc2-119">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="d5dc2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5dc2-120">-ResourceGroupName</span></span>
<span data-ttu-id="d5dc2-121">계정을 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-121">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="d5dc2-122">리소스 그룹이 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-122">The resource group must already exist.</span></span>

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

### <span data-ttu-id="d5dc2-123">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="d5dc2-123">-SkuName</span></span>
<span data-ttu-id="d5dc2-124">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-124">Specifies the SKU for the account.</span></span>
<span data-ttu-id="d5dc2-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5dc2-126">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="d5dc2-126">F0 (free tier)</span></span>
- <span data-ttu-id="d5dc2-127">S0</span><span class="sxs-lookup"><span data-stu-id="d5dc2-127">S0</span></span>
- <span data-ttu-id="d5dc2-128">S1</span><span class="sxs-lookup"><span data-stu-id="d5dc2-128">S1</span></span>
- <span data-ttu-id="d5dc2-129">구성원과</span><span class="sxs-lookup"><span data-stu-id="d5dc2-129">S2</span></span>
- <span data-ttu-id="d5dc2-130">시스템이</span><span class="sxs-lookup"><span data-stu-id="d5dc2-130">S3</span></span>
- <span data-ttu-id="d5dc2-131">S4 자세한 내용은 [인식 서비스 api](https://www.microsoft.com/cognitive-services/en-us/apis)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-131">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="d5dc2-132">태그</span><span class="sxs-lookup"><span data-stu-id="d5dc2-132">-Tag</span></span>
<span data-ttu-id="d5dc2-133">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-133">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="d5dc2-134">-Type</span><span class="sxs-lookup"><span data-stu-id="d5dc2-134">-Type</span></span>
<span data-ttu-id="d5dc2-135">만들 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-135">Specifies the type of account to create.</span></span> <span data-ttu-id="d5dc2-136">`Get-AzCognitiveServicesAccountType`Cmdlet을 사용 하 여 현재 허용 되는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-136">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="d5dc2-137">-확인</span><span class="sxs-lookup"><span data-stu-id="d5dc2-137">-Confirm</span></span>
<span data-ttu-id="d5dc2-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5dc2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5dc2-139">-WhatIf</span></span>
<span data-ttu-id="d5dc2-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5dc2-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5dc2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5dc2-142">CommonParameters</span></span>
<span data-ttu-id="d5dc2-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5dc2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5dc2-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5dc2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5dc2-145">입력</span><span class="sxs-lookup"><span data-stu-id="d5dc2-145">INPUTS</span></span>

### <span data-ttu-id="d5dc2-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5dc2-146">System.String</span></span>

## <span data-ttu-id="d5dc2-147">출력</span><span class="sxs-lookup"><span data-stu-id="d5dc2-147">OUTPUTS</span></span>

### <span data-ttu-id="d5dc2-148">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="d5dc2-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="d5dc2-149">상속자</span><span class="sxs-lookup"><span data-stu-id="d5dc2-149">NOTES</span></span>

## <span data-ttu-id="d5dc2-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5dc2-150">RELATED LINKS</span></span>

[<span data-ttu-id="d5dc2-151">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d5dc2-151">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="d5dc2-152">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d5dc2-152">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="d5dc2-153">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d5dc2-153">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
