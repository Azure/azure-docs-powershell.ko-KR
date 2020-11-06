---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536096"
---
# <span data-ttu-id="31092-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="31092-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="31092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31092-102">SYNOPSIS</span></span>
<span data-ttu-id="31092-103">계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31092-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31092-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31092-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31092-105">DESCRIPTION</span></span>
<span data-ttu-id="31092-106">**AzureRmCognitiveServicesAccount** cmdlet은 지정 된 인식 서비스 계정의 SKU 또는 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="31092-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31092-107">EXAMPLES</span></span>

## <span data-ttu-id="31092-108">변수</span><span class="sxs-lookup"><span data-stu-id="31092-108">PARAMETERS</span></span>

### <span data-ttu-id="31092-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31092-109">-DefaultProfile</span></span>
<span data-ttu-id="31092-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="31092-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31092-111">-Force</span><span class="sxs-lookup"><span data-stu-id="31092-111">-Force</span></span>
<span data-ttu-id="31092-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31092-113">-이름</span><span class="sxs-lookup"><span data-stu-id="31092-113">-Name</span></span>
<span data-ttu-id="31092-114">수정할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-114">Specifies the name of the account to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31092-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31092-115">-ResourceGroupName</span></span>
<span data-ttu-id="31092-116">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31092-117">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="31092-117">-SkuName</span></span>
<span data-ttu-id="31092-118">계정에 대 한 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="31092-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="31092-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31092-120">F0 (free 티어)</span><span class="sxs-lookup"><span data-stu-id="31092-120">F0 (free tier)</span></span>
- <span data-ttu-id="31092-121">S0</span><span class="sxs-lookup"><span data-stu-id="31092-121">S0</span></span>
- <span data-ttu-id="31092-122">S1</span><span class="sxs-lookup"><span data-stu-id="31092-122">S1</span></span>
- <span data-ttu-id="31092-123">구성원과</span><span class="sxs-lookup"><span data-stu-id="31092-123">S2</span></span>
- <span data-ttu-id="31092-124">시스템이</span><span class="sxs-lookup"><span data-stu-id="31092-124">S3</span></span>
- <span data-ttu-id="31092-125">S4</span><span class="sxs-lookup"><span data-stu-id="31092-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31092-126">태그</span><span class="sxs-lookup"><span data-stu-id="31092-126">-Tag</span></span>
<span data-ttu-id="31092-127">태그를 이름/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31092-128">-확인</span><span class="sxs-lookup"><span data-stu-id="31092-128">-Confirm</span></span>
<span data-ttu-id="31092-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31092-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31092-130">-WhatIf</span></span>
<span data-ttu-id="31092-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31092-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31092-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31092-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31092-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31092-133">CommonParameters</span></span>
<span data-ttu-id="31092-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31092-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31092-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31092-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31092-136">입력</span><span class="sxs-lookup"><span data-stu-id="31092-136">INPUTS</span></span>

### <span data-ttu-id="31092-137">않아야</span><span class="sxs-lookup"><span data-stu-id="31092-137">None</span></span>
<span data-ttu-id="31092-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31092-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31092-139">출력</span><span class="sxs-lookup"><span data-stu-id="31092-139">OUTPUTS</span></span>

### <span data-ttu-id="31092-140">CognitiveServices. PSCognitiveServicesAccount/. \*</span><span class="sxs-lookup"><span data-stu-id="31092-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="31092-141">상속자</span><span class="sxs-lookup"><span data-stu-id="31092-141">NOTES</span></span>

## <span data-ttu-id="31092-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31092-142">RELATED LINKS</span></span>

[<span data-ttu-id="31092-143">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="31092-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="31092-144">새로운 AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="31092-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="31092-145">제거-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="31092-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
