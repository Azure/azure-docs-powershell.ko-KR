---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: fcfd642ceaf2f371385ee1f09c99e1efa566941d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006624"
---
# <span data-ttu-id="193dd-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="193dd-101">Get-AzMediaService</span></span>

## <span data-ttu-id="193dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="193dd-102">SYNOPSIS</span></span>
<span data-ttu-id="193dd-103">미디어 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="193dd-103">Gets information about a media service.</span></span>

## <span data-ttu-id="193dd-104">구문</span><span class="sxs-lookup"><span data-stu-id="193dd-104">SYNTAX</span></span>

### <span data-ttu-id="193dd-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="193dd-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="193dd-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="193dd-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="193dd-107">설명</span><span class="sxs-lookup"><span data-stu-id="193dd-107">DESCRIPTION</span></span>
<span data-ttu-id="193dd-108">**Get-AzMediaService** cmdlet은 미디어 서비스에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="193dd-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="193dd-109">예제</span><span class="sxs-lookup"><span data-stu-id="193dd-109">EXAMPLES</span></span>

### <span data-ttu-id="193dd-110">예제 1: 리소스 그룹의 모든 미디어 서비스 사용</span><span class="sxs-lookup"><span data-stu-id="193dd-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="193dd-111">이 명령은 ResourceGroup001이라는 리소스 그룹의 모든 미디어 서비스에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="193dd-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="193dd-112">예제 2: 미디어 서비스 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="193dd-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="193dd-113">이 명령은 ResourceGroup002라는 리소스 그룹에 속하는 MediaService1이라는 미디어 서비스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="193dd-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="193dd-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="193dd-114">PARAMETERS</span></span>

### <span data-ttu-id="193dd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="193dd-115">-AccountName</span></span>
<span data-ttu-id="193dd-116">이 cmdlet이 제공하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="193dd-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="193dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="193dd-117">-DefaultProfile</span></span>
<span data-ttu-id="193dd-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="193dd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="193dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="193dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="193dd-120">미디어 서비스를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="193dd-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="193dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="193dd-121">CommonParameters</span></span>
<span data-ttu-id="193dd-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="193dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="193dd-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="193dd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="193dd-124">입력</span><span class="sxs-lookup"><span data-stu-id="193dd-124">INPUTS</span></span>

### <span data-ttu-id="193dd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="193dd-125">System.String</span></span>

## <span data-ttu-id="193dd-126">출력</span><span class="sxs-lookup"><span data-stu-id="193dd-126">OUTPUTS</span></span>

### <span data-ttu-id="193dd-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="193dd-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="193dd-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="193dd-128">NOTES</span></span>

## <span data-ttu-id="193dd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="193dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="193dd-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="193dd-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="193dd-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="193dd-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="193dd-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="193dd-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


