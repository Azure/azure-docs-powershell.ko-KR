---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 451498760d85cc018b8fbade625625ec6ecc1910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528450"
---
# <span data-ttu-id="96b45-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="96b45-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="96b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96b45-102">SYNOPSIS</span></span>
<span data-ttu-id="96b45-103">다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96b45-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96b45-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96b45-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96b45-105">DESCRIPTION</span></span>
<span data-ttu-id="96b45-106">Save-AzureRmContext cmdlet은 다른 PowerShell 세션에서 사용할 현재 인증 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="96b45-107">예제의</span><span class="sxs-lookup"><span data-stu-id="96b45-107">EXAMPLES</span></span>

### <span data-ttu-id="96b45-108">예제 1: 현재 세션의 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="96b45-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="96b45-109">이 예제에서는 현재 세션의 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="96b45-110">예제 2: 지정 된 컨텍스트 저장</span><span class="sxs-lookup"><span data-stu-id="96b45-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="96b45-111">이 예제에서는 cmdlet에 전달 된 Azure 컨텍스트를 제공 된 JSON 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="96b45-112">변수</span><span class="sxs-lookup"><span data-stu-id="96b45-112">PARAMETERS</span></span>

### <span data-ttu-id="96b45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b45-113">-DefaultProfile</span></span>
<span data-ttu-id="96b45-114">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b45-115">-Force</span><span class="sxs-lookup"><span data-stu-id="96b45-115">-Force</span></span>
<span data-ttu-id="96b45-116">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="96b45-117">-Path</span><span class="sxs-lookup"><span data-stu-id="96b45-117">-Path</span></span>
<span data-ttu-id="96b45-118">인증 정보를 저장할 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b45-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="96b45-119">-Profile</span></span>
<span data-ttu-id="96b45-120">이 cmdlet이 읽는 Azure 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="96b45-121">컨텍스트를 지정 하지 않으면이 cmdlet은 로컬 기본 컨텍스트를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96b45-122">-확인</span><span class="sxs-lookup"><span data-stu-id="96b45-122">-Confirm</span></span>
<span data-ttu-id="96b45-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b45-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b45-124">-WhatIf</span></span>
<span data-ttu-id="96b45-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96b45-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b45-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b45-127">CommonParameters</span></span>
<span data-ttu-id="96b45-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96b45-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b45-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96b45-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b45-130">입력</span><span class="sxs-lookup"><span data-stu-id="96b45-130">INPUTS</span></span>

### <span data-ttu-id="96b45-131">AzureRmProfile (일반. 인증. 모델)</span><span class="sxs-lookup"><span data-stu-id="96b45-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>
<span data-ttu-id="96b45-132">매개 변수: Profile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96b45-132">Parameters: Profile (ByValue)</span></span>

## <span data-ttu-id="96b45-133">출력</span><span class="sxs-lookup"><span data-stu-id="96b45-133">OUTPUTS</span></span>

### <span data-ttu-id="96b45-134">Microsoft. Azure. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="96b45-134">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="96b45-135">상속자</span><span class="sxs-lookup"><span data-stu-id="96b45-135">NOTES</span></span>

## <span data-ttu-id="96b45-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96b45-136">RELATED LINKS</span></span>
