---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: d19c22ffd0be5b6ea935b832d847bb74661e3106
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697542"
---
# <span data-ttu-id="69e86-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="69e86-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="69e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69e86-102">SYNOPSIS</span></span>
<span data-ttu-id="69e86-103">인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="69e86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69e86-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69e86-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69e86-105">DESCRIPTION</span></span>
<span data-ttu-id="69e86-106">**AzCognitiveServicesAccount** cmdlet은 지정 된 형식 및 SKU의 인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-106">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="69e86-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69e86-107">EXAMPLES</span></span>

### <span data-ttu-id="69e86-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="69e86-108">1:</span></span>
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

## <span data-ttu-id="69e86-109">변수</span><span class="sxs-lookup"><span data-stu-id="69e86-109">PARAMETERS</span></span>

### <span data-ttu-id="69e86-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="69e86-110">-CustomSubdomainName</span></span>
<span data-ttu-id="69e86-111">인지 서비스 계정 하위 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="69e86-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e86-112">-DefaultProfile</span></span>
<span data-ttu-id="69e86-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="69e86-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69e86-114">-Force</span><span class="sxs-lookup"><span data-stu-id="69e86-114">-Force</span></span>
<span data-ttu-id="69e86-115">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69e86-116">-위치</span><span class="sxs-lookup"><span data-stu-id="69e86-116">-Location</span></span>
<span data-ttu-id="69e86-117">계정을 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-117">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="69e86-118">-이름</span><span class="sxs-lookup"><span data-stu-id="69e86-118">-Name</span></span>
<span data-ttu-id="69e86-119">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-119">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="69e86-120">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="69e86-120">-NetworkRuleSet</span></span>
<span data-ttu-id="69e86-121">NetworkRuleSet는 방화벽 및 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 방법 등의 네트워크 속성에 대 한 값을 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-121">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e86-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e86-122">-ResourceGroupName</span></span>
<span data-ttu-id="69e86-123">계정을 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-123">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="69e86-124">리소스 그룹이 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-124">The resource group must already exist.</span></span>

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

### <span data-ttu-id="69e86-125">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="69e86-125">-SkuName</span></span>
<span data-ttu-id="69e86-126">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-126">Specifies the SKU for the account.</span></span>
<span data-ttu-id="69e86-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69e86-128">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="69e86-128">F0 (free tier)</span></span>
- <span data-ttu-id="69e86-129">S0</span><span class="sxs-lookup"><span data-stu-id="69e86-129">S0</span></span>
- <span data-ttu-id="69e86-130">S1</span><span class="sxs-lookup"><span data-stu-id="69e86-130">S1</span></span>
- <span data-ttu-id="69e86-131">구성원과</span><span class="sxs-lookup"><span data-stu-id="69e86-131">S2</span></span>
- <span data-ttu-id="69e86-132">시스템이</span><span class="sxs-lookup"><span data-stu-id="69e86-132">S3</span></span>
- <span data-ttu-id="69e86-133">S4 자세한 내용은 [인식 서비스 api](https://www.microsoft.com/cognitive-services/en-us/apis)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69e86-133">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="69e86-134">태그</span><span class="sxs-lookup"><span data-stu-id="69e86-134">-Tag</span></span>
<span data-ttu-id="69e86-135">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-135">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="69e86-136">-Type</span><span class="sxs-lookup"><span data-stu-id="69e86-136">-Type</span></span>
<span data-ttu-id="69e86-137">만들 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-137">Specifies the type of account to create.</span></span> <span data-ttu-id="69e86-138">`Get-AzCognitiveServicesAccountType`Cmdlet을 사용 하 여 현재 허용 되는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-138">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="69e86-139">-확인</span><span class="sxs-lookup"><span data-stu-id="69e86-139">-Confirm</span></span>
<span data-ttu-id="69e86-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69e86-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e86-141">-WhatIf</span></span>
<span data-ttu-id="69e86-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69e86-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69e86-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e86-144">CommonParameters</span></span>
<span data-ttu-id="69e86-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69e86-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e86-146">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69e86-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e86-147">입력</span><span class="sxs-lookup"><span data-stu-id="69e86-147">INPUTS</span></span>

### <span data-ttu-id="69e86-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69e86-148">System.String</span></span>

## <span data-ttu-id="69e86-149">출력</span><span class="sxs-lookup"><span data-stu-id="69e86-149">OUTPUTS</span></span>

### <span data-ttu-id="69e86-150">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="69e86-150">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="69e86-151">상속자</span><span class="sxs-lookup"><span data-stu-id="69e86-151">NOTES</span></span>

## <span data-ttu-id="69e86-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69e86-152">RELATED LINKS</span></span>

[<span data-ttu-id="69e86-153">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="69e86-153">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="69e86-154">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="69e86-154">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="69e86-155">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="69e86-155">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
