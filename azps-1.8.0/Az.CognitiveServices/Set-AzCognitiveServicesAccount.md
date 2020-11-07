---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701387"
---
# <span data-ttu-id="00f99-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="00f99-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="00f99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f99-102">SYNOPSIS</span></span>
<span data-ttu-id="00f99-103">계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-103">Modifies an account.</span></span>

## <span data-ttu-id="00f99-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00f99-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00f99-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00f99-105">DESCRIPTION</span></span>
<span data-ttu-id="00f99-106">**AzCognitiveServicesAccount** cmdlet은 지정 된 인식 서비스 계정의 SKU 또는 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="00f99-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00f99-107">EXAMPLES</span></span>

### <span data-ttu-id="00f99-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="00f99-108">Example 1</span></span>
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

## <span data-ttu-id="00f99-109">변수</span><span class="sxs-lookup"><span data-stu-id="00f99-109">PARAMETERS</span></span>

### <span data-ttu-id="00f99-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f99-110">-DefaultProfile</span></span>
<span data-ttu-id="00f99-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="00f99-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00f99-112">-Force</span><span class="sxs-lookup"><span data-stu-id="00f99-112">-Force</span></span>
<span data-ttu-id="00f99-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00f99-114">-이름</span><span class="sxs-lookup"><span data-stu-id="00f99-114">-Name</span></span>
<span data-ttu-id="00f99-115">수정할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="00f99-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f99-116">-ResourceGroupName</span></span>
<span data-ttu-id="00f99-117">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="00f99-118">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="00f99-118">-SkuName</span></span>
<span data-ttu-id="00f99-119">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="00f99-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="00f99-121">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="00f99-121">F0 (free tier)</span></span>
- <span data-ttu-id="00f99-122">S0</span><span class="sxs-lookup"><span data-stu-id="00f99-122">S0</span></span>
- <span data-ttu-id="00f99-123">S1</span><span class="sxs-lookup"><span data-stu-id="00f99-123">S1</span></span>
- <span data-ttu-id="00f99-124">구성원과</span><span class="sxs-lookup"><span data-stu-id="00f99-124">S2</span></span>
- <span data-ttu-id="00f99-125">시스템이</span><span class="sxs-lookup"><span data-stu-id="00f99-125">S3</span></span>
- <span data-ttu-id="00f99-126">S4</span><span class="sxs-lookup"><span data-stu-id="00f99-126">S4</span></span>

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

### <span data-ttu-id="00f99-127">태그</span><span class="sxs-lookup"><span data-stu-id="00f99-127">-Tag</span></span>
<span data-ttu-id="00f99-128">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-128">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="00f99-129">-확인</span><span class="sxs-lookup"><span data-stu-id="00f99-129">-Confirm</span></span>
<span data-ttu-id="00f99-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00f99-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00f99-131">-WhatIf</span></span>
<span data-ttu-id="00f99-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00f99-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00f99-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f99-134">CommonParameters</span></span>
<span data-ttu-id="00f99-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f99-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f99-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f99-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f99-137">입력</span><span class="sxs-lookup"><span data-stu-id="00f99-137">INPUTS</span></span>

### <span data-ttu-id="00f99-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00f99-138">System.String</span></span>

### <span data-ttu-id="00f99-139">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="00f99-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="00f99-140">출력</span><span class="sxs-lookup"><span data-stu-id="00f99-140">OUTPUTS</span></span>

### <span data-ttu-id="00f99-141">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="00f99-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="00f99-142">상속자</span><span class="sxs-lookup"><span data-stu-id="00f99-142">NOTES</span></span>

## <span data-ttu-id="00f99-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00f99-143">RELATED LINKS</span></span>

[<span data-ttu-id="00f99-144">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="00f99-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="00f99-145">새로운 AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="00f99-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="00f99-146">제거-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="00f99-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
