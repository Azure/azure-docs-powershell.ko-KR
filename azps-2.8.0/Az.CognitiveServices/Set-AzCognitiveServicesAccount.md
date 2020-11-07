---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 57d136691d6ca0ac9bcd85f205d70cf267437b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697533"
---
# <span data-ttu-id="bb82e-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb82e-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="bb82e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb82e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb82e-103">계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-103">Modifies an account.</span></span>

## <span data-ttu-id="bb82e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb82e-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb82e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb82e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb82e-106">**AzCognitiveServicesAccount** cmdlet은 지정 된 인식 서비스 계정의 SKU 또는 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="bb82e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bb82e-107">EXAMPLES</span></span>

### <span data-ttu-id="bb82e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb82e-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="bb82e-109">변수</span><span class="sxs-lookup"><span data-stu-id="bb82e-109">PARAMETERS</span></span>

### <span data-ttu-id="bb82e-110">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="bb82e-110">-CustomSubdomainName</span></span>
<span data-ttu-id="bb82e-111">인지 서비스 계정 하위 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-111">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="bb82e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb82e-112">-DefaultProfile</span></span>
<span data-ttu-id="bb82e-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bb82e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb82e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="bb82e-114">-Force</span></span>
<span data-ttu-id="bb82e-115">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bb82e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="bb82e-116">-Name</span></span>
<span data-ttu-id="bb82e-117">수정할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-117">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="bb82e-118">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="bb82e-118">-NetworkRuleSet</span></span>
<span data-ttu-id="bb82e-119">NetworkRuleSet는 방화벽 및 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 방법 등의 네트워크 속성에 대 한 값을 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-119">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="bb82e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb82e-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb82e-121">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="bb82e-122">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="bb82e-122">-SkuName</span></span>
<span data-ttu-id="bb82e-123">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-123">Specifies the SKU for the account.</span></span>
<span data-ttu-id="bb82e-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb82e-125">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="bb82e-125">F0 (free tier)</span></span>
- <span data-ttu-id="bb82e-126">S0</span><span class="sxs-lookup"><span data-stu-id="bb82e-126">S0</span></span>
- <span data-ttu-id="bb82e-127">S1</span><span class="sxs-lookup"><span data-stu-id="bb82e-127">S1</span></span>
- <span data-ttu-id="bb82e-128">구성원과</span><span class="sxs-lookup"><span data-stu-id="bb82e-128">S2</span></span>
- <span data-ttu-id="bb82e-129">시스템이</span><span class="sxs-lookup"><span data-stu-id="bb82e-129">S3</span></span>
- <span data-ttu-id="bb82e-130">S4</span><span class="sxs-lookup"><span data-stu-id="bb82e-130">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb82e-131">태그</span><span class="sxs-lookup"><span data-stu-id="bb82e-131">-Tag</span></span>
<span data-ttu-id="bb82e-132">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb82e-133">-확인</span><span class="sxs-lookup"><span data-stu-id="bb82e-133">-Confirm</span></span>
<span data-ttu-id="bb82e-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb82e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb82e-135">-WhatIf</span></span>
<span data-ttu-id="bb82e-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb82e-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb82e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb82e-138">CommonParameters</span></span>
<span data-ttu-id="bb82e-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb82e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb82e-140">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb82e-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb82e-141">입력</span><span class="sxs-lookup"><span data-stu-id="bb82e-141">INPUTS</span></span>

### <span data-ttu-id="bb82e-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bb82e-142">System.String</span></span>

### <span data-ttu-id="bb82e-143">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="bb82e-143">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="bb82e-144">출력</span><span class="sxs-lookup"><span data-stu-id="bb82e-144">OUTPUTS</span></span>

### <span data-ttu-id="bb82e-145">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="bb82e-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="bb82e-146">상속자</span><span class="sxs-lookup"><span data-stu-id="bb82e-146">NOTES</span></span>

## <span data-ttu-id="bb82e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb82e-147">RELATED LINKS</span></span>

[<span data-ttu-id="bb82e-148">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb82e-148">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="bb82e-149">새로운 AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb82e-149">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="bb82e-150">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bb82e-150">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
