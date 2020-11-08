---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: fc510ebede11168dd8d8b090cd2069ce3e6de52c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033762"
---
# <span data-ttu-id="7a5f9-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a5f9-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="7a5f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a5f9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5f9-103">계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-103">Modifies an account.</span></span>

## <span data-ttu-id="7a5f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a5f9-104">SYNTAX</span></span>

### <span data-ttu-id="7a5f9-105">CognitiveServicesEncryption (기본값)</span><span class="sxs-lookup"><span data-stu-id="7a5f9-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a5f9-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7a5f9-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a5f9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7a5f9-107">DESCRIPTION</span></span>
<span data-ttu-id="7a5f9-108">**AzCognitiveServicesAccount** cmdlet은 지정 된 인식 서비스 계정의 SKU 또는 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="7a5f9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7a5f9-109">EXAMPLES</span></span>

### <span data-ttu-id="7a5f9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a5f9-110">Example 1</span></span>
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

## <span data-ttu-id="7a5f9-111">변수</span><span class="sxs-lookup"><span data-stu-id="7a5f9-111">PARAMETERS</span></span>

### <span data-ttu-id="7a5f9-112">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="7a5f9-112">-AssignIdentity</span></span>
<span data-ttu-id="7a5f9-113">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 인식 서비스 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7a5f9-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="7a5f9-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="7a5f9-115">인지 서비스 계정 암호화 KeySource를 Microsoft CognitiveServices로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="7a5f9-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="7a5f9-116">-CustomSubdomainName</span></span>
<span data-ttu-id="7a5f9-117">인지 서비스 계정 하위 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="7a5f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5f9-118">-DefaultProfile</span></span>
<span data-ttu-id="7a5f9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7a5f9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a5f9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7a5f9-120">-Force</span></span>
<span data-ttu-id="7a5f9-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a5f9-122">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7a5f9-122">-IdentityType</span></span>
<span data-ttu-id="7a5f9-123">관리 되는 서비스 id의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-123">Type of managed service identity.</span></span>

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

### <span data-ttu-id="7a5f9-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7a5f9-124">-KeyName</span></span>
<span data-ttu-id="7a5f9-125">인식 서비스 계정 암호화 keySource Keysource KeyName</span><span class="sxs-lookup"><span data-stu-id="7a5f9-125">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="7a5f9-126">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7a5f9-126">-KeyVaultEncryption</span></span>
<span data-ttu-id="7a5f9-127">인식 서비스 계정 암호화 keySource를 Microsoft. Keysource로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-127">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="7a5f9-128">KeyName, KeyVersion 및 KeyVaultUri를 지정 하면 인식 서비스 계정 암호화 키 원본도 Microsoft로 설정 됩니다. Keyversion 날씨이 매개 변수는 설정 되거나 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-128">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="7a5f9-129">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7a5f9-129">-KeyVaultUri</span></span>
<span data-ttu-id="7a5f9-130">인식 서비스 계정 암호화 keySource Keysource KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7a5f9-130">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="7a5f9-131">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="7a5f9-131">-KeyVersion</span></span>
<span data-ttu-id="7a5f9-132">인식 서비스 계정 암호화 keySource Keysource Keysource</span><span class="sxs-lookup"><span data-stu-id="7a5f9-132">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="7a5f9-133">-이름</span><span class="sxs-lookup"><span data-stu-id="7a5f9-133">-Name</span></span>
<span data-ttu-id="7a5f9-134">수정할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-134">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="7a5f9-135">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="7a5f9-135">-NetworkRuleSet</span></span>
<span data-ttu-id="7a5f9-136">NetworkRuleSet는 방화벽 및 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 방법 등의 네트워크 속성에 대 한 값을 설정 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="7a5f9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a5f9-137">-ResourceGroupName</span></span>
<span data-ttu-id="7a5f9-138">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-138">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="7a5f9-139">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="7a5f9-139">-SkuName</span></span>
<span data-ttu-id="7a5f9-140">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-140">Specifies the SKU for the account.</span></span>
<span data-ttu-id="7a5f9-141">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7a5f9-142">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="7a5f9-142">F0 (free tier)</span></span>
- <span data-ttu-id="7a5f9-143">S0</span><span class="sxs-lookup"><span data-stu-id="7a5f9-143">S0</span></span>
- <span data-ttu-id="7a5f9-144">S1</span><span class="sxs-lookup"><span data-stu-id="7a5f9-144">S1</span></span>
- <span data-ttu-id="7a5f9-145">구성원과</span><span class="sxs-lookup"><span data-stu-id="7a5f9-145">S2</span></span>
- <span data-ttu-id="7a5f9-146">시스템이</span><span class="sxs-lookup"><span data-stu-id="7a5f9-146">S3</span></span>
- <span data-ttu-id="7a5f9-147">S4</span><span class="sxs-lookup"><span data-stu-id="7a5f9-147">S4</span></span>

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

### <span data-ttu-id="7a5f9-148">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7a5f9-148">-StorageAccountId</span></span>
<span data-ttu-id="7a5f9-149">사용자 소유의 저장소 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-149">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="7a5f9-150">태그</span><span class="sxs-lookup"><span data-stu-id="7a5f9-150">-Tag</span></span>
<span data-ttu-id="7a5f9-151">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-151">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="7a5f9-152">-확인</span><span class="sxs-lookup"><span data-stu-id="7a5f9-152">-Confirm</span></span>
<span data-ttu-id="7a5f9-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a5f9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a5f9-154">-WhatIf</span></span>
<span data-ttu-id="7a5f9-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a5f9-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a5f9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5f9-157">CommonParameters</span></span>
<span data-ttu-id="7a5f9-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5f9-159">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a5f9-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5f9-160">입력</span><span class="sxs-lookup"><span data-stu-id="7a5f9-160">INPUTS</span></span>

### <span data-ttu-id="7a5f9-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7a5f9-161">System.String</span></span>

### <span data-ttu-id="7a5f9-162">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="7a5f9-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="7a5f9-163">출력</span><span class="sxs-lookup"><span data-stu-id="7a5f9-163">OUTPUTS</span></span>

### <span data-ttu-id="7a5f9-164">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="7a5f9-164">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="7a5f9-165">상속자</span><span class="sxs-lookup"><span data-stu-id="7a5f9-165">NOTES</span></span>

## <span data-ttu-id="7a5f9-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a5f9-166">RELATED LINKS</span></span>

[<span data-ttu-id="7a5f9-167">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a5f9-167">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7a5f9-168">새로운 AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a5f9-168">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7a5f9-169">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a5f9-169">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
