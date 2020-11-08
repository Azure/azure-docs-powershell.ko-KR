---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213685"
---
# <span data-ttu-id="1489b-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1489b-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="1489b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1489b-102">SYNOPSIS</span></span>
<span data-ttu-id="1489b-103">인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="1489b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1489b-104">SYNTAX</span></span>

### <span data-ttu-id="1489b-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="1489b-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1489b-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="1489b-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1489b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1489b-107">DESCRIPTION</span></span>
<span data-ttu-id="1489b-108">**AzCognitiveServicesAccount** cmdlet은 지정 된 형식 및 SKU의 인지 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="1489b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1489b-109">EXAMPLES</span></span>

### <span data-ttu-id="1489b-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="1489b-110">1:</span></span>
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

## <span data-ttu-id="1489b-111">변수</span><span class="sxs-lookup"><span data-stu-id="1489b-111">PARAMETERS</span></span>

### <span data-ttu-id="1489b-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="1489b-112">-ApiProperty</span></span>
<span data-ttu-id="1489b-113">인지 서비스 계정의 ApiProperties입니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="1489b-114">특정 계정 유형에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="1489b-115">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="1489b-115">-AssignIdentity</span></span>
<span data-ttu-id="1489b-116">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 인식 서비스 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1489b-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="1489b-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="1489b-118">인지 서비스 계정 암호화 KeySource를 Microsoft CognitiveServices로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="1489b-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="1489b-119">-CustomSubdomainName</span></span>
<span data-ttu-id="1489b-120">인지 서비스 계정 하위 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="1489b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1489b-121">-DefaultProfile</span></span>
<span data-ttu-id="1489b-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1489b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1489b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1489b-123">-Force</span></span>
<span data-ttu-id="1489b-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1489b-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1489b-125">-KeyName</span></span>
<span data-ttu-id="1489b-126">인식 서비스 계정 암호화 keySource Keysource KeyName</span><span class="sxs-lookup"><span data-stu-id="1489b-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="1489b-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="1489b-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="1489b-128">인식 서비스 계정 암호화 keySource를 Microsoft. Keysource로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="1489b-129">KeyName, KeyVersion 및 KeyVaultUri를 지정 하면 인식 서비스 계정 암호화 키 원본도 Microsoft로 설정 됩니다. Keyversion 날씨이 매개 변수는 설정 되거나 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="1489b-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1489b-130">-KeyVaultUri</span></span>
<span data-ttu-id="1489b-131">인식 서비스 계정 암호화 keySource Keysource KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1489b-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="1489b-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="1489b-132">-KeyVersion</span></span>
<span data-ttu-id="1489b-133">인식 서비스 계정 암호화 keySource Keysource Keysource</span><span class="sxs-lookup"><span data-stu-id="1489b-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="1489b-134">-위치</span><span class="sxs-lookup"><span data-stu-id="1489b-134">-Location</span></span>
<span data-ttu-id="1489b-135">계정을 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="1489b-136">-이름</span><span class="sxs-lookup"><span data-stu-id="1489b-136">-Name</span></span>
<span data-ttu-id="1489b-137">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="1489b-138">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="1489b-138">-NetworkRuleSet</span></span>
<span data-ttu-id="1489b-139">NetworkRuleSet는 방화벽 및 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 방법 등의 네트워크 속성에 대 한 값을 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="1489b-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="1489b-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="1489b-141">인지 서비스 계정에 대 한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="1489b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1489b-142">-ResourceGroupName</span></span>
<span data-ttu-id="1489b-143">계정을 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="1489b-144">리소스 그룹이 이미 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="1489b-145">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="1489b-145">-SkuName</span></span>
<span data-ttu-id="1489b-146">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="1489b-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1489b-148">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="1489b-148">F0 (free tier)</span></span>
- <span data-ttu-id="1489b-149">S0</span><span class="sxs-lookup"><span data-stu-id="1489b-149">S0</span></span>
- <span data-ttu-id="1489b-150">S1</span><span class="sxs-lookup"><span data-stu-id="1489b-150">S1</span></span>
- <span data-ttu-id="1489b-151">구성원과</span><span class="sxs-lookup"><span data-stu-id="1489b-151">S2</span></span>
- <span data-ttu-id="1489b-152">시스템이</span><span class="sxs-lookup"><span data-stu-id="1489b-152">S3</span></span>
- <span data-ttu-id="1489b-153">S4 자세한 내용은 [인식 서비스 api](https://www.microsoft.com/cognitive-services/en-us/apis)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1489b-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="1489b-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1489b-154">-StorageAccountId</span></span>
<span data-ttu-id="1489b-155">사용자 소유의 저장소 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="1489b-156">태그</span><span class="sxs-lookup"><span data-stu-id="1489b-156">-Tag</span></span>
<span data-ttu-id="1489b-157">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="1489b-158">-Type</span><span class="sxs-lookup"><span data-stu-id="1489b-158">-Type</span></span>
<span data-ttu-id="1489b-159">만들 계정의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-159">Specifies the type of account to create.</span></span> <span data-ttu-id="1489b-160">`Get-AzCognitiveServicesAccountType`Cmdlet을 사용 하 여 현재 허용 되는 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="1489b-161">-확인</span><span class="sxs-lookup"><span data-stu-id="1489b-161">-Confirm</span></span>
<span data-ttu-id="1489b-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1489b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1489b-163">-WhatIf</span></span>
<span data-ttu-id="1489b-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1489b-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1489b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1489b-166">CommonParameters</span></span>
<span data-ttu-id="1489b-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1489b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1489b-168">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1489b-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1489b-169">입력</span><span class="sxs-lookup"><span data-stu-id="1489b-169">INPUTS</span></span>

### <span data-ttu-id="1489b-170">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1489b-170">System.String</span></span>

## <span data-ttu-id="1489b-171">출력</span><span class="sxs-lookup"><span data-stu-id="1489b-171">OUTPUTS</span></span>

### <span data-ttu-id="1489b-172">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="1489b-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="1489b-173">상속자</span><span class="sxs-lookup"><span data-stu-id="1489b-173">NOTES</span></span>

## <span data-ttu-id="1489b-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1489b-174">RELATED LINKS</span></span>

[<span data-ttu-id="1489b-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1489b-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="1489b-176">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1489b-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="1489b-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1489b-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
