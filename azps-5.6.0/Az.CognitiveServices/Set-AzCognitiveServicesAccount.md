---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2c995157b56bafb56df7b385c250b6f7c4fdd4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991685"
---
# <span data-ttu-id="1885a-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1885a-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="1885a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1885a-102">SYNOPSIS</span></span>
<span data-ttu-id="1885a-103">계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-103">Modifies an account.</span></span>

## <span data-ttu-id="1885a-104">구문</span><span class="sxs-lookup"><span data-stu-id="1885a-104">SYNTAX</span></span>

### <span data-ttu-id="1885a-105">CognitiveServicesEncryption(기본값)</span><span class="sxs-lookup"><span data-stu-id="1885a-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1885a-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="1885a-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1885a-107">설명</span><span class="sxs-lookup"><span data-stu-id="1885a-107">DESCRIPTION</span></span>
<span data-ttu-id="1885a-108">**Set-AzCognitiveServicesAccount** cmdlet은 지정된 Cognitive Services 계정의 SKU 또는 태그를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="1885a-109">예제</span><span class="sxs-lookup"><span data-stu-id="1885a-109">EXAMPLES</span></span>

### <span data-ttu-id="1885a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1885a-110">Example 1</span></span>
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

## <span data-ttu-id="1885a-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1885a-111">PARAMETERS</span></span>

### <span data-ttu-id="1885a-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="1885a-112">-ApiProperty</span></span>
<span data-ttu-id="1885a-113">Cognitive Services 계정의 ApiProperties입니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="1885a-114">특정 계정 유형에 따라 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="1885a-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1885a-115">-AssignIdentity</span></span>
<span data-ttu-id="1885a-116">Azure KeyVault와 같은 주요 관리 서비스와 함께 사용하기 위해 이 저장소 계정에 대한 새 Cognitive Services 계정 ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1885a-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="1885a-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="1885a-118">Cognitive Services 계정 암호화 KeySource를 Microsoft.CognitiveServices로 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="1885a-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="1885a-119">-CustomSubdomainName</span></span>
<span data-ttu-id="1885a-120">Cognitive Services 계정 하위omain 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="1885a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1885a-121">-DefaultProfile</span></span>
<span data-ttu-id="1885a-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1885a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1885a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1885a-123">-Force</span></span>
<span data-ttu-id="1885a-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1885a-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1885a-125">-IdentityType</span></span>
<span data-ttu-id="1885a-126">관리되는 서비스 ID 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1885a-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1885a-127">-KeyName</span></span>
<span data-ttu-id="1885a-128">Cognitive Services 계정 암호화 키Source KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="1885a-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="1885a-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="1885a-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="1885a-130">Cognitive Services 계정 암호화 키를 설정할지 여부Source를 Microsoft.KeyVault로 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="1885a-131">KeyName, KeyVersion 및 KeyVaultUri를 지정하는 경우 Cognitive Services 계정 암호화 KeySource도 Microsoft.KeyVault 날씨로 설정됩니다. 이 매개 변수는 설정되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="1885a-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1885a-132">-KeyVaultUri</span></span>
<span data-ttu-id="1885a-133">Cognitive Services 계정 암호화 키Source KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1885a-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="1885a-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="1885a-134">-KeyVersion</span></span>
<span data-ttu-id="1885a-135">Cognitive Services 계정 암호화 키Source KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="1885a-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="1885a-136">-Name</span><span class="sxs-lookup"><span data-stu-id="1885a-136">-Name</span></span>
<span data-ttu-id="1885a-137">수정할 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="1885a-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1885a-138">-NetworkRuleSet</span></span>
<span data-ttu-id="1885a-139">NetworkRuleSet은 방화벽 및 가상 네트워크에 대한 구성 규칙 집합을 정의하고 정의된 규칙과 일치하지 않는 요청을 처리하는 방법과 같은 네트워크 속성에 대한 값을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="1885a-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="1885a-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="1885a-141">Cognitive Services 계정에 대한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="1885a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1885a-142">-ResourceGroupName</span></span>
<span data-ttu-id="1885a-143">계정에 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="1885a-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1885a-144">-SkuName</span></span>
<span data-ttu-id="1885a-145">계정에 대한 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="1885a-146">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1885a-147">F0(무료 계층)</span><span class="sxs-lookup"><span data-stu-id="1885a-147">F0 (free tier)</span></span>
- <span data-ttu-id="1885a-148">S0</span><span class="sxs-lookup"><span data-stu-id="1885a-148">S0</span></span>
- <span data-ttu-id="1885a-149">S1</span><span class="sxs-lookup"><span data-stu-id="1885a-149">S1</span></span>
- <span data-ttu-id="1885a-150">S2</span><span class="sxs-lookup"><span data-stu-id="1885a-150">S2</span></span>
- <span data-ttu-id="1885a-151">S3</span><span class="sxs-lookup"><span data-stu-id="1885a-151">S3</span></span>
- <span data-ttu-id="1885a-152">S4</span><span class="sxs-lookup"><span data-stu-id="1885a-152">S4</span></span>

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

### <span data-ttu-id="1885a-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1885a-153">-StorageAccountId</span></span>
<span data-ttu-id="1885a-154">사용자 소유 저장소 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="1885a-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="1885a-155">-Tag</span></span>
<span data-ttu-id="1885a-156">태그를 이름/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="1885a-157">-확인</span><span class="sxs-lookup"><span data-stu-id="1885a-157">-Confirm</span></span>
<span data-ttu-id="1885a-158">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1885a-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1885a-159">-WhatIf</span></span>
<span data-ttu-id="1885a-160">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1885a-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1885a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1885a-162">CommonParameters</span></span>
<span data-ttu-id="1885a-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1885a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1885a-164">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1885a-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1885a-165">입력</span><span class="sxs-lookup"><span data-stu-id="1885a-165">INPUTS</span></span>

### <span data-ttu-id="1885a-166">System.String</span><span class="sxs-lookup"><span data-stu-id="1885a-166">System.String</span></span>

### <span data-ttu-id="1885a-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="1885a-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="1885a-168">출력</span><span class="sxs-lookup"><span data-stu-id="1885a-168">OUTPUTS</span></span>

### <span data-ttu-id="1885a-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1885a-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="1885a-170">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1885a-170">NOTES</span></span>

## <span data-ttu-id="1885a-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1885a-171">RELATED LINKS</span></span>

[<span data-ttu-id="1885a-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1885a-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="1885a-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1885a-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="1885a-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1885a-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
