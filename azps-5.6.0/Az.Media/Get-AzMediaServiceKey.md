---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: 59f288c74c8f5230375a475df839c491e07e58d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996618"
---
# <span data-ttu-id="9ccca-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="9ccca-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="9ccca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ccca-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccca-103">미디어 서비스와 연결된 REST 엔드포인트에 액세스하기 위한 주요 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ccca-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="9ccca-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ccca-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ccca-105">설명</span><span class="sxs-lookup"><span data-stu-id="9ccca-105">DESCRIPTION</span></span>
<span data-ttu-id="9ccca-106">**Get-AzMediaServiceKey** cmdlet은 Azure 미디어 서비스에 연결된 REST(표현 상태 전송) 엔드포인트에 액세스하기 위한 주요 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccca-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="9ccca-107">예제</span><span class="sxs-lookup"><span data-stu-id="9ccca-107">EXAMPLES</span></span>

### <span data-ttu-id="9ccca-108">예제 1: 미디어 서비스에 액세스하기 위한 주요 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ccca-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="9ccca-109">이 명령은 ResourceGroup001이라는 리소스 그룹에 속하는 MediaService001이라는 미디어 서비스에 액세스하기 위한 주요 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ccca-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="9ccca-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9ccca-110">PARAMETERS</span></span>

### <span data-ttu-id="9ccca-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9ccca-111">-AccountName</span></span>
<span data-ttu-id="9ccca-112">이 cmdlet에서 미디어 서비스 키를 얻게 하는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccca-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ccca-113">-DefaultProfile</span></span>
<span data-ttu-id="9ccca-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9ccca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ccca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ccca-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ccca-116">미디어 서비스를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccca-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="9ccca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccca-117">CommonParameters</span></span>
<span data-ttu-id="9ccca-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ccca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccca-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9ccca-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccca-120">입력</span><span class="sxs-lookup"><span data-stu-id="9ccca-120">INPUTS</span></span>

### <span data-ttu-id="9ccca-121">System.String</span><span class="sxs-lookup"><span data-stu-id="9ccca-121">System.String</span></span>

## <span data-ttu-id="9ccca-122">출력</span><span class="sxs-lookup"><span data-stu-id="9ccca-122">OUTPUTS</span></span>

### <span data-ttu-id="9ccca-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="9ccca-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="9ccca-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ccca-124">NOTES</span></span>

## <span data-ttu-id="9ccca-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ccca-125">RELATED LINKS</span></span>

[<span data-ttu-id="9ccca-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="9ccca-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


