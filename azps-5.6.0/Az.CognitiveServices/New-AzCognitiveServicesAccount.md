---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: e6ed6669c98a54a037bcbdc579e08459cdff568e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981200"
---
# <span data-ttu-id="26c59-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26c59-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="26c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26c59-102">SYNOPSIS</span></span>
<span data-ttu-id="26c59-103">Cognitive Services 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="26c59-104">구문</span><span class="sxs-lookup"><span data-stu-id="26c59-104">SYNTAX</span></span>

### <span data-ttu-id="26c59-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="26c59-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c59-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="26c59-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c59-107">설명</span><span class="sxs-lookup"><span data-stu-id="26c59-107">DESCRIPTION</span></span>
<span data-ttu-id="26c59-108">**New-AzCognitiveServicesAccount** cmdlet은 지정된 형식 및 SKU가 있는 Cognitive Services 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="26c59-109">예제</span><span class="sxs-lookup"><span data-stu-id="26c59-109">EXAMPLES</span></span>

### <span data-ttu-id="26c59-110">1:</span><span class="sxs-lookup"><span data-stu-id="26c59-110">1:</span></span>
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

## <span data-ttu-id="26c59-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="26c59-111">PARAMETERS</span></span>

### <span data-ttu-id="26c59-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="26c59-112">-ApiProperty</span></span>
<span data-ttu-id="26c59-113">Cognitive Services 계정의 ApiProperties입니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="26c59-114">특정 계정 유형에 따라 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c59-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="26c59-115">-AssignIdentity</span></span>
<span data-ttu-id="26c59-116">Azure KeyVault와 같은 주요 관리 서비스와 함께 사용하기 위해 이 저장소 계정에 대한 새 Cognitive Services 계정 ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="26c59-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="26c59-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="26c59-118">Cognitive Services 계정 암호화 KeySource를 Microsoft.CognitiveServices로 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="26c59-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="26c59-119">-CustomSubdomainName</span></span>
<span data-ttu-id="26c59-120">Cognitive Services 계정 하위omain 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="26c59-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c59-121">-DefaultProfile</span></span>
<span data-ttu-id="26c59-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26c59-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26c59-123">-Force</span><span class="sxs-lookup"><span data-stu-id="26c59-123">-Force</span></span>
<span data-ttu-id="26c59-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26c59-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="26c59-125">-KeyName</span></span>
<span data-ttu-id="26c59-126">Cognitive Services 계정 암호화 키Source KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="26c59-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="26c59-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="26c59-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="26c59-128">Cognitive Services 계정 암호화 키를 설정할지 여부Source를 Microsoft.KeyVault로 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="26c59-129">KeyName, KeyVersion 및 KeyVaultUri를 지정하는 경우 Cognitive Services 계정 암호화 KeySource도 Microsoft.KeyVault 날씨로 설정됩니다. 이 매개 변수는 설정되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="26c59-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="26c59-130">-KeyVaultUri</span></span>
<span data-ttu-id="26c59-131">Cognitive Services 계정 암호화 키Source KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="26c59-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="26c59-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="26c59-132">-KeyVersion</span></span>
<span data-ttu-id="26c59-133">Cognitive Services 계정 암호화 키Source KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="26c59-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="26c59-134">-Location</span><span class="sxs-lookup"><span data-stu-id="26c59-134">-Location</span></span>
<span data-ttu-id="26c59-135">계정을 만들 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="26c59-136">-Name</span><span class="sxs-lookup"><span data-stu-id="26c59-136">-Name</span></span>
<span data-ttu-id="26c59-137">계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="26c59-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="26c59-138">-NetworkRuleSet</span></span>
<span data-ttu-id="26c59-139">NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="26c59-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="26c59-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="26c59-141">Cognitive Services 계정에 대한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c59-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c59-142">-ResourceGroupName</span></span>
<span data-ttu-id="26c59-143">계정을 할당할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="26c59-144">리소스 그룹이 이미 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="26c59-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="26c59-145">-SkuName</span></span>
<span data-ttu-id="26c59-146">계정에 대한 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="26c59-147">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="26c59-148">F0(무료 계층)</span><span class="sxs-lookup"><span data-stu-id="26c59-148">F0 (free tier)</span></span>
- <span data-ttu-id="26c59-149">S0</span><span class="sxs-lookup"><span data-stu-id="26c59-149">S0</span></span>
- <span data-ttu-id="26c59-150">S1</span><span class="sxs-lookup"><span data-stu-id="26c59-150">S1</span></span>
- <span data-ttu-id="26c59-151">S2</span><span class="sxs-lookup"><span data-stu-id="26c59-151">S2</span></span>
- <span data-ttu-id="26c59-152">S3</span><span class="sxs-lookup"><span data-stu-id="26c59-152">S3</span></span>
- <span data-ttu-id="26c59-153">S4 자세한 내용은 [Cognitive Service API 를 참조하세요.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="26c59-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="26c59-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="26c59-154">-StorageAccountId</span></span>
<span data-ttu-id="26c59-155">사용자 소유 저장소 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="26c59-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="26c59-156">-Tag</span></span>
<span data-ttu-id="26c59-157">태그를 이름/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="26c59-158">-Type</span><span class="sxs-lookup"><span data-stu-id="26c59-158">-Type</span></span>
<span data-ttu-id="26c59-159">만들 계정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-159">Specifies the type of account to create.</span></span> <span data-ttu-id="26c59-160">`Get-AzCognitiveServicesAccountType`cmdlet을 사용하여 현재 허용 가능한 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="26c59-161">-확인</span><span class="sxs-lookup"><span data-stu-id="26c59-161">-Confirm</span></span>
<span data-ttu-id="26c59-162">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c59-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c59-163">-WhatIf</span></span>
<span data-ttu-id="26c59-164">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26c59-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c59-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c59-166">CommonParameters</span></span>
<span data-ttu-id="26c59-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26c59-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c59-168">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26c59-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c59-169">입력</span><span class="sxs-lookup"><span data-stu-id="26c59-169">INPUTS</span></span>

### <span data-ttu-id="26c59-170">System.String</span><span class="sxs-lookup"><span data-stu-id="26c59-170">System.String</span></span>

## <span data-ttu-id="26c59-171">출력</span><span class="sxs-lookup"><span data-stu-id="26c59-171">OUTPUTS</span></span>

### <span data-ttu-id="26c59-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26c59-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="26c59-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26c59-173">NOTES</span></span>

## <span data-ttu-id="26c59-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26c59-174">RELATED LINKS</span></span>

[<span data-ttu-id="26c59-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26c59-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="26c59-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26c59-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="26c59-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="26c59-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
