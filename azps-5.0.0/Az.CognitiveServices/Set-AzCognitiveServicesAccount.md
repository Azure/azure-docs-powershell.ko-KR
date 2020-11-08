---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219091"
---
# <span data-ttu-id="63c73-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="63c73-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="63c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63c73-102">SYNOPSIS</span></span>
<span data-ttu-id="63c73-103">계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-103">Modifies an account.</span></span>

## <span data-ttu-id="63c73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63c73-104">SYNTAX</span></span>

### <span data-ttu-id="63c73-105">CognitiveServicesEncryption (기본값)</span><span class="sxs-lookup"><span data-stu-id="63c73-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63c73-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="63c73-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63c73-107">설명은</span><span class="sxs-lookup"><span data-stu-id="63c73-107">DESCRIPTION</span></span>
<span data-ttu-id="63c73-108">**AzCognitiveServicesAccount** cmdlet은 지정 된 인식 서비스 계정의 SKU 또는 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="63c73-109">예제의</span><span class="sxs-lookup"><span data-stu-id="63c73-109">EXAMPLES</span></span>

### <span data-ttu-id="63c73-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="63c73-110">Example 1</span></span>
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

## <span data-ttu-id="63c73-111">변수</span><span class="sxs-lookup"><span data-stu-id="63c73-111">PARAMETERS</span></span>

### <span data-ttu-id="63c73-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="63c73-112">-ApiProperty</span></span>
<span data-ttu-id="63c73-113">인지 서비스 계정의 ApiProperties입니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="63c73-114">특정 계정 유형에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="63c73-115">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="63c73-115">-AssignIdentity</span></span>
<span data-ttu-id="63c73-116">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 인식 서비스 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="63c73-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="63c73-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="63c73-118">인지 서비스 계정 암호화 KeySource를 Microsoft CognitiveServices로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="63c73-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="63c73-119">-CustomSubdomainName</span></span>
<span data-ttu-id="63c73-120">인지 서비스 계정 하위 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="63c73-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c73-121">-DefaultProfile</span></span>
<span data-ttu-id="63c73-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="63c73-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63c73-123">-Force</span><span class="sxs-lookup"><span data-stu-id="63c73-123">-Force</span></span>
<span data-ttu-id="63c73-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="63c73-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="63c73-125">-IdentityType</span></span>
<span data-ttu-id="63c73-126">관리 되는 서비스 id의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-126">Type of managed service identity.</span></span>

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

### <span data-ttu-id="63c73-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="63c73-127">-KeyName</span></span>
<span data-ttu-id="63c73-128">인식 서비스 계정 암호화 keySource Keysource KeyName</span><span class="sxs-lookup"><span data-stu-id="63c73-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="63c73-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="63c73-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="63c73-130">인식 서비스 계정 암호화 keySource를 Microsoft. Keysource로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="63c73-131">KeyName, KeyVersion 및 KeyVaultUri를 지정 하면 인식 서비스 계정 암호화 키 원본도 Microsoft로 설정 됩니다. Keyversion 날씨이 매개 변수는 설정 되거나 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="63c73-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="63c73-132">-KeyVaultUri</span></span>
<span data-ttu-id="63c73-133">인식 서비스 계정 암호화 keySource Keysource KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="63c73-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="63c73-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="63c73-134">-KeyVersion</span></span>
<span data-ttu-id="63c73-135">인식 서비스 계정 암호화 keySource Keysource Keysource</span><span class="sxs-lookup"><span data-stu-id="63c73-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="63c73-136">-이름</span><span class="sxs-lookup"><span data-stu-id="63c73-136">-Name</span></span>
<span data-ttu-id="63c73-137">수정할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="63c73-138">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="63c73-138">-NetworkRuleSet</span></span>
<span data-ttu-id="63c73-139">NetworkRuleSet는 방화벽 및 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 방법 등의 네트워크 속성에 대 한 값을 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="63c73-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="63c73-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="63c73-141">인지 서비스 계정에 대 한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="63c73-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63c73-142">-ResourceGroupName</span></span>
<span data-ttu-id="63c73-143">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="63c73-144">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="63c73-144">-SkuName</span></span>
<span data-ttu-id="63c73-145">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="63c73-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="63c73-147">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="63c73-147">F0 (free tier)</span></span>
- <span data-ttu-id="63c73-148">S0</span><span class="sxs-lookup"><span data-stu-id="63c73-148">S0</span></span>
- <span data-ttu-id="63c73-149">S1</span><span class="sxs-lookup"><span data-stu-id="63c73-149">S1</span></span>
- <span data-ttu-id="63c73-150">구성원과</span><span class="sxs-lookup"><span data-stu-id="63c73-150">S2</span></span>
- <span data-ttu-id="63c73-151">시스템이</span><span class="sxs-lookup"><span data-stu-id="63c73-151">S3</span></span>
- <span data-ttu-id="63c73-152">S4</span><span class="sxs-lookup"><span data-stu-id="63c73-152">S4</span></span>

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

### <span data-ttu-id="63c73-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="63c73-153">-StorageAccountId</span></span>
<span data-ttu-id="63c73-154">사용자 소유의 저장소 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="63c73-155">태그</span><span class="sxs-lookup"><span data-stu-id="63c73-155">-Tag</span></span>
<span data-ttu-id="63c73-156">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="63c73-157">-확인</span><span class="sxs-lookup"><span data-stu-id="63c73-157">-Confirm</span></span>
<span data-ttu-id="63c73-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63c73-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63c73-159">-WhatIf</span></span>
<span data-ttu-id="63c73-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63c73-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63c73-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c73-162">CommonParameters</span></span>
<span data-ttu-id="63c73-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c73-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c73-164">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="63c73-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c73-165">입력</span><span class="sxs-lookup"><span data-stu-id="63c73-165">INPUTS</span></span>

### <span data-ttu-id="63c73-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63c73-166">System.String</span></span>

### <span data-ttu-id="63c73-167">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="63c73-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="63c73-168">출력</span><span class="sxs-lookup"><span data-stu-id="63c73-168">OUTPUTS</span></span>

### <span data-ttu-id="63c73-169">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="63c73-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="63c73-170">상속자</span><span class="sxs-lookup"><span data-stu-id="63c73-170">NOTES</span></span>

## <span data-ttu-id="63c73-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63c73-171">RELATED LINKS</span></span>

[<span data-ttu-id="63c73-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="63c73-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="63c73-173">새로운 AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="63c73-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="63c73-174">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="63c73-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
