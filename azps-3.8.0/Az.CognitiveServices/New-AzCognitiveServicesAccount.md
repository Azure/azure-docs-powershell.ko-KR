---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033775"
---
# <span data-ttu-id="9ca18-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9ca18-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="9ca18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca18-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca18-103">인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="9ca18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ca18-104">SYNTAX</span></span>

### <span data-ttu-id="9ca18-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="9ca18-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ca18-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="9ca18-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca18-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9ca18-107">DESCRIPTION</span></span>
<span data-ttu-id="9ca18-108">**AzCognitiveServicesAccount** cmdlet은 지정 된 형식 및 SKU의 인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="9ca18-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9ca18-109">EXAMPLES</span></span>

### <span data-ttu-id="9ca18-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="9ca18-110">1:</span></span>
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

## <span data-ttu-id="9ca18-111">변수</span><span class="sxs-lookup"><span data-stu-id="9ca18-111">PARAMETERS</span></span>

### <span data-ttu-id="9ca18-112">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="9ca18-112">-AssignIdentity</span></span>
<span data-ttu-id="9ca18-113">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 인식 서비스 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9ca18-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="9ca18-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="9ca18-115">인지 서비스 계정 암호화 KeySource를 Microsoft CognitiveServices로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca18-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="9ca18-116">-CustomSubdomainName</span></span>
<span data-ttu-id="9ca18-117">인지 서비스 계정 하위 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="9ca18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca18-118">-DefaultProfile</span></span>
<span data-ttu-id="9ca18-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9ca18-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ca18-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9ca18-120">-Force</span></span>
<span data-ttu-id="9ca18-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ca18-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9ca18-122">-KeyName</span></span>
<span data-ttu-id="9ca18-123">인식 서비스 계정 암호화 keySource Keysource KeyName</span><span class="sxs-lookup"><span data-stu-id="9ca18-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca18-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="9ca18-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="9ca18-125">인식 서비스 계정 암호화 keySource를 Microsoft. Keysource로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="9ca18-126">KeyName, KeyVersion 및 KeyVaultUri를 지정 하면 인식 서비스 계정 암호화 키 원본도 Microsoft로 설정 됩니다. Keyversion 날씨이 매개 변수는 설정 되거나 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca18-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="9ca18-127">-KeyVaultUri</span></span>
<span data-ttu-id="9ca18-128">인식 서비스 계정 암호화 keySource Keysource KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="9ca18-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca18-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="9ca18-129">-KeyVersion</span></span>
<span data-ttu-id="9ca18-130">인식 서비스 계정 암호화 keySource Keysource Keysource</span><span class="sxs-lookup"><span data-stu-id="9ca18-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca18-131">-위치</span><span class="sxs-lookup"><span data-stu-id="9ca18-131">-Location</span></span>
<span data-ttu-id="9ca18-132">계정을 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-132">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="9ca18-133">-이름</span><span class="sxs-lookup"><span data-stu-id="9ca18-133">-Name</span></span>
<span data-ttu-id="9ca18-134">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="9ca18-135">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="9ca18-135">-NetworkRuleSet</span></span>
<span data-ttu-id="9ca18-136">NetworkRuleSet는 방화벽 및 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 방법 등의 네트워크 속성에 대 한 값을 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="9ca18-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ca18-137">-ResourceGroupName</span></span>
<span data-ttu-id="9ca18-138">계정을 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="9ca18-139">리소스 그룹이 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="9ca18-140">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="9ca18-140">-SkuName</span></span>
<span data-ttu-id="9ca18-141">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="9ca18-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ca18-143">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="9ca18-143">F0 (free tier)</span></span>
- <span data-ttu-id="9ca18-144">S0</span><span class="sxs-lookup"><span data-stu-id="9ca18-144">S0</span></span>
- <span data-ttu-id="9ca18-145">S1</span><span class="sxs-lookup"><span data-stu-id="9ca18-145">S1</span></span>
- <span data-ttu-id="9ca18-146">구성원과</span><span class="sxs-lookup"><span data-stu-id="9ca18-146">S2</span></span>
- <span data-ttu-id="9ca18-147">시스템이</span><span class="sxs-lookup"><span data-stu-id="9ca18-147">S3</span></span>
- <span data-ttu-id="9ca18-148">S4 자세한 내용은 [인식 서비스 api](https://www.microsoft.com/cognitive-services/en-us/apis)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ca18-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="9ca18-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9ca18-149">-StorageAccountId</span></span>
<span data-ttu-id="9ca18-150">사용자 소유의 저장소 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-150">List of User Owned Storage Accounts.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca18-151">태그</span><span class="sxs-lookup"><span data-stu-id="9ca18-151">-Tag</span></span>
<span data-ttu-id="9ca18-152">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-152">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="9ca18-153">-Type</span><span class="sxs-lookup"><span data-stu-id="9ca18-153">-Type</span></span>
<span data-ttu-id="9ca18-154">만들 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-154">Specifies the type of account to create.</span></span> <span data-ttu-id="9ca18-155">`Get-AzCognitiveServicesAccountType`Cmdlet을 사용 하 여 현재 허용 되는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="9ca18-156">-확인</span><span class="sxs-lookup"><span data-stu-id="9ca18-156">-Confirm</span></span>
<span data-ttu-id="9ca18-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ca18-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca18-158">-WhatIf</span></span>
<span data-ttu-id="9ca18-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ca18-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ca18-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca18-161">CommonParameters</span></span>
<span data-ttu-id="9ca18-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca18-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca18-163">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ca18-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca18-164">입력</span><span class="sxs-lookup"><span data-stu-id="9ca18-164">INPUTS</span></span>

### <span data-ttu-id="9ca18-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ca18-165">System.String</span></span>

## <span data-ttu-id="9ca18-166">출력</span><span class="sxs-lookup"><span data-stu-id="9ca18-166">OUTPUTS</span></span>

### <span data-ttu-id="9ca18-167">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="9ca18-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="9ca18-168">상속자</span><span class="sxs-lookup"><span data-stu-id="9ca18-168">NOTES</span></span>

## <span data-ttu-id="9ca18-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ca18-169">RELATED LINKS</span></span>

[<span data-ttu-id="9ca18-170">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9ca18-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="9ca18-171">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9ca18-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="9ca18-172">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9ca18-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
