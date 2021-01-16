---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326857"
---
# <span data-ttu-id="a29db-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a29db-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="a29db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a29db-102">SYNOPSIS</span></span>
<span data-ttu-id="a29db-103">Cognitive Services 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="a29db-104">구문</span><span class="sxs-lookup"><span data-stu-id="a29db-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a29db-105">설명</span><span class="sxs-lookup"><span data-stu-id="a29db-105">DESCRIPTION</span></span>
<span data-ttu-id="a29db-106">**Remove-AzCognitiveServicesAccount** cmdlet은 지정된 Cognitive Services 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="a29db-107">예제</span><span class="sxs-lookup"><span data-stu-id="a29db-107">EXAMPLES</span></span>

### <span data-ttu-id="a29db-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a29db-108">Example 1</span></span>
<span data-ttu-id="a29db-109">이 명령은 아무 것도 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="a29db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a29db-110">PARAMETERS</span></span>

### <span data-ttu-id="a29db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29db-111">-DefaultProfile</span></span>
<span data-ttu-id="a29db-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a29db-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a29db-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a29db-113">-Force</span></span>
<span data-ttu-id="a29db-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a29db-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a29db-115">-Name</span></span>
<span data-ttu-id="a29db-116">삭제할 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="a29db-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a29db-117">-ResourceGroupName</span></span>
<span data-ttu-id="a29db-118">Cognitive Services 계정이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="a29db-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a29db-119">-Confirm</span></span>
<span data-ttu-id="a29db-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a29db-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a29db-121">-WhatIf</span></span>
<span data-ttu-id="a29db-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a29db-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a29db-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a29db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29db-124">CommonParameters</span></span>
<span data-ttu-id="a29db-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a29db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29db-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a29db-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29db-127">입력</span><span class="sxs-lookup"><span data-stu-id="a29db-127">INPUTS</span></span>

### <span data-ttu-id="a29db-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a29db-128">System.String</span></span>

## <span data-ttu-id="a29db-129">출력</span><span class="sxs-lookup"><span data-stu-id="a29db-129">OUTPUTS</span></span>

### <span data-ttu-id="a29db-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="a29db-130">System.Void</span></span>

## <span data-ttu-id="a29db-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a29db-131">NOTES</span></span>

## <span data-ttu-id="a29db-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a29db-132">RELATED LINKS</span></span>

[<span data-ttu-id="a29db-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a29db-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="a29db-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a29db-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="a29db-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a29db-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)

