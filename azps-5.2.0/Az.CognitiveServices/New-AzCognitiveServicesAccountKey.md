---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346065"
---
# <span data-ttu-id="155b8-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="155b8-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="155b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="155b8-102">SYNOPSIS</span></span>
<span data-ttu-id="155b8-103">계정 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-103">Regenerates an account key.</span></span>

## <span data-ttu-id="155b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="155b8-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="155b8-105">설명</span><span class="sxs-lookup"><span data-stu-id="155b8-105">DESCRIPTION</span></span>
<span data-ttu-id="155b8-106">**New-AzCognitiveServicesAccountKey** cmdlet은 Cognitive Services 계정에 대한 API 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="155b8-107">예제</span><span class="sxs-lookup"><span data-stu-id="155b8-107">EXAMPLES</span></span>

### <span data-ttu-id="155b8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="155b8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="155b8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="155b8-109">PARAMETERS</span></span>

### <span data-ttu-id="155b8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155b8-110">-DefaultProfile</span></span>
<span data-ttu-id="155b8-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="155b8-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="155b8-112">-Force</span><span class="sxs-lookup"><span data-stu-id="155b8-112">-Force</span></span>
<span data-ttu-id="155b8-113">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="155b8-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="155b8-114">-KeyName</span></span>
<span data-ttu-id="155b8-115">다시 생성하는 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="155b8-116">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="155b8-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="155b8-117">Key1</span><span class="sxs-lookup"><span data-stu-id="155b8-117">Key1</span></span>
- <span data-ttu-id="155b8-118">Key2</span><span class="sxs-lookup"><span data-stu-id="155b8-118">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases:
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="155b8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="155b8-119">-Name</span></span>
<span data-ttu-id="155b8-120">계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="155b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="155b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="155b8-122">계정이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="155b8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="155b8-123">-Confirm</span></span>
<span data-ttu-id="155b8-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="155b8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="155b8-125">-WhatIf</span></span>
<span data-ttu-id="155b8-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="155b8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="155b8-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="155b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155b8-128">CommonParameters</span></span>
<span data-ttu-id="155b8-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="155b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155b8-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="155b8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155b8-131">입력</span><span class="sxs-lookup"><span data-stu-id="155b8-131">INPUTS</span></span>

### <span data-ttu-id="155b8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="155b8-132">System.String</span></span>

### <span data-ttu-id="155b8-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span><span class="sxs-lookup"><span data-stu-id="155b8-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="155b8-134">출력</span><span class="sxs-lookup"><span data-stu-id="155b8-134">OUTPUTS</span></span>

### <span data-ttu-id="155b8-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="155b8-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="155b8-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="155b8-136">NOTES</span></span>

## <span data-ttu-id="155b8-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="155b8-137">RELATED LINKS</span></span>

[<span data-ttu-id="155b8-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="155b8-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


