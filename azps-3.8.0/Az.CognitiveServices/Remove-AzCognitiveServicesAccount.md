---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033763"
---
# <span data-ttu-id="8e9ff-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e9ff-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="8e9ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9ff-103">인지 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="8e9ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e9ff-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e9ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e9ff-105">DESCRIPTION</span></span>
<span data-ttu-id="8e9ff-106">**AzCognitiveServicesAccount** cmdlet은 지정 된 인식 서비스 계정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="8e9ff-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e9ff-107">EXAMPLES</span></span>

### <span data-ttu-id="8e9ff-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e9ff-108">Example 1</span></span>
<span data-ttu-id="8e9ff-109">이 명령은 아무것도 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="8e9ff-110">변수</span><span class="sxs-lookup"><span data-stu-id="8e9ff-110">PARAMETERS</span></span>

### <span data-ttu-id="8e9ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9ff-111">-DefaultProfile</span></span>
<span data-ttu-id="8e9ff-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8e9ff-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e9ff-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8e9ff-113">-Force</span></span>
<span data-ttu-id="8e9ff-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e9ff-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8e9ff-115">-Name</span></span>
<span data-ttu-id="8e9ff-116">삭제할 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="8e9ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e9ff-118">인지 서비스 계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="8e9ff-119">-확인</span><span class="sxs-lookup"><span data-stu-id="8e9ff-119">-Confirm</span></span>
<span data-ttu-id="8e9ff-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9ff-121">-WhatIf</span></span>
<span data-ttu-id="8e9ff-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9ff-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9ff-124">CommonParameters</span></span>
<span data-ttu-id="8e9ff-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9ff-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e9ff-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9ff-127">입력</span><span class="sxs-lookup"><span data-stu-id="8e9ff-127">INPUTS</span></span>

### <span data-ttu-id="8e9ff-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e9ff-128">System.String</span></span>

## <span data-ttu-id="8e9ff-129">출력</span><span class="sxs-lookup"><span data-stu-id="8e9ff-129">OUTPUTS</span></span>

### <span data-ttu-id="8e9ff-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="8e9ff-130">System.Void</span></span>

## <span data-ttu-id="8e9ff-131">상속자</span><span class="sxs-lookup"><span data-stu-id="8e9ff-131">NOTES</span></span>

## <span data-ttu-id="8e9ff-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e9ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e9ff-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e9ff-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8e9ff-134">새로운 AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e9ff-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8e9ff-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e9ff-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


