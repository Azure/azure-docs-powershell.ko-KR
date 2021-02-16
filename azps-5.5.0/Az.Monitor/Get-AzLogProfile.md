---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180172"
---
# <span data-ttu-id="5b207-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="5b207-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="5b207-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b207-102">SYNOPSIS</span></span>
<span data-ttu-id="5b207-103">로그 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b207-103">Gets a log profile.</span></span>

## <span data-ttu-id="5b207-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b207-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b207-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b207-105">DESCRIPTION</span></span>
<span data-ttu-id="5b207-106">**Get-AzLogProfile** cmdlet은 로그 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b207-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="5b207-107">예제</span><span class="sxs-lookup"><span data-stu-id="5b207-107">EXAMPLES</span></span>

## <span data-ttu-id="5b207-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b207-108">PARAMETERS</span></span>

### <span data-ttu-id="5b207-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b207-109">-DefaultProfile</span></span>
<span data-ttu-id="5b207-110">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5b207-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b207-111">-Name</span><span class="sxs-lookup"><span data-stu-id="5b207-111">-Name</span></span>
<span data-ttu-id="5b207-112">얻을 로그 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b207-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="5b207-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b207-113">CommonParameters</span></span>
<span data-ttu-id="5b207-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b207-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b207-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b207-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b207-116">입력</span><span class="sxs-lookup"><span data-stu-id="5b207-116">INPUTS</span></span>

### <span data-ttu-id="5b207-117">System.String</span><span class="sxs-lookup"><span data-stu-id="5b207-117">System.String</span></span>

## <span data-ttu-id="5b207-118">출력</span><span class="sxs-lookup"><span data-stu-id="5b207-118">OUTPUTS</span></span>

### <span data-ttu-id="5b207-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="5b207-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="5b207-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b207-120">NOTES</span></span>

## <span data-ttu-id="5b207-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b207-121">RELATED LINKS</span></span>

[<span data-ttu-id="5b207-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="5b207-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="5b207-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="5b207-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


