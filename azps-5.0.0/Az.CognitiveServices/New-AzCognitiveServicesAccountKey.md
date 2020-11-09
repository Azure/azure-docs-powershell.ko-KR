---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307406"
---
# <span data-ttu-id="3fca2-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3fca2-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="3fca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fca2-102">SYNOPSIS</span></span>
<span data-ttu-id="3fca2-103">계정 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-103">Regenerates an account key.</span></span>

## <span data-ttu-id="3fca2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3fca2-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fca2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3fca2-105">DESCRIPTION</span></span>
<span data-ttu-id="3fca2-106">**AzCognitiveServicesAccountKey** Cmdlet은 인지 서비스 계정에 대 한 API 키를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="3fca2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3fca2-107">EXAMPLES</span></span>

### <span data-ttu-id="3fca2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3fca2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="3fca2-109">변수</span><span class="sxs-lookup"><span data-stu-id="3fca2-109">PARAMETERS</span></span>

### <span data-ttu-id="3fca2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fca2-110">-DefaultProfile</span></span>
<span data-ttu-id="3fca2-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3fca2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fca2-112">-Force</span><span class="sxs-lookup"><span data-stu-id="3fca2-112">-Force</span></span>
<span data-ttu-id="3fca2-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3fca2-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3fca2-114">-KeyName</span></span>
<span data-ttu-id="3fca2-115">다시 생성할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="3fca2-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3fca2-117">Key1</span><span class="sxs-lookup"><span data-stu-id="3fca2-117">Key1</span></span>
- <span data-ttu-id="3fca2-118">Key2</span><span class="sxs-lookup"><span data-stu-id="3fca2-118">Key2</span></span>

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

### <span data-ttu-id="3fca2-119">-이름</span><span class="sxs-lookup"><span data-stu-id="3fca2-119">-Name</span></span>
<span data-ttu-id="3fca2-120">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="3fca2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fca2-121">-ResourceGroupName</span></span>
<span data-ttu-id="3fca2-122">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="3fca2-123">-확인</span><span class="sxs-lookup"><span data-stu-id="3fca2-123">-Confirm</span></span>
<span data-ttu-id="3fca2-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fca2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fca2-125">-WhatIf</span></span>
<span data-ttu-id="3fca2-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fca2-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fca2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fca2-128">CommonParameters</span></span>
<span data-ttu-id="3fca2-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3fca2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fca2-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3fca2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fca2-131">입력</span><span class="sxs-lookup"><span data-stu-id="3fca2-131">INPUTS</span></span>

### <span data-ttu-id="3fca2-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3fca2-132">System.String</span></span>

### <span data-ttu-id="3fca2-133">CognitiveServices. m a.</span><span class="sxs-lookup"><span data-stu-id="3fca2-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="3fca2-134">출력</span><span class="sxs-lookup"><span data-stu-id="3fca2-134">OUTPUTS</span></span>

### <span data-ttu-id="3fca2-135">CognitiveServices. CognitiveServicesAccountKeys/.</span><span class="sxs-lookup"><span data-stu-id="3fca2-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="3fca2-136">상속자</span><span class="sxs-lookup"><span data-stu-id="3fca2-136">NOTES</span></span>

## <span data-ttu-id="3fca2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fca2-137">RELATED LINKS</span></span>

[<span data-ttu-id="3fca2-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3fca2-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


