---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 8b1f4a10ab974f50a01ba0725285ccd7a3b7dffc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703043"
---
# <span data-ttu-id="f36db-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="f36db-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="f36db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f36db-102">SYNOPSIS</span></span>
<span data-ttu-id="f36db-103">미디어 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f36db-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f36db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f36db-104">SYNTAX</span></span>

### <span data-ttu-id="f36db-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f36db-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f36db-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f36db-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f36db-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f36db-107">DESCRIPTION</span></span>
<span data-ttu-id="f36db-108">**AzureRmMediaService** cmdlet은 미디어 서비스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f36db-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="f36db-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f36db-109">EXAMPLES</span></span>

### <span data-ttu-id="f36db-110">예제 1: 리소스 그룹의 모든 미디어 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="f36db-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="f36db-111">이 명령은 ResourceGroup001 이라는 리소스 그룹의 모든 미디어 서비스에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f36db-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f36db-112">예제 2: 미디어 서비스 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="f36db-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="f36db-113">이 명령은 ResourceGroup002 이라는 리소스 그룹에 속하는 MediaService1 이라는 미디어 서비스의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f36db-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f36db-114">변수</span><span class="sxs-lookup"><span data-stu-id="f36db-114">PARAMETERS</span></span>

### <span data-ttu-id="f36db-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f36db-115">-AccountName</span></span>
<span data-ttu-id="f36db-116">이 cmdlet이 가져오는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36db-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f36db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36db-117">-DefaultProfile</span></span>
<span data-ttu-id="f36db-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f36db-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f36db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36db-119">-ResourceGroupName</span></span>
<span data-ttu-id="f36db-120">미디어 서비스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36db-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f36db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36db-121">CommonParameters</span></span>
<span data-ttu-id="f36db-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f36db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36db-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f36db-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36db-124">입력</span><span class="sxs-lookup"><span data-stu-id="f36db-124">INPUTS</span></span>

### <span data-ttu-id="f36db-125">않아야</span><span class="sxs-lookup"><span data-stu-id="f36db-125">None</span></span>
<span data-ttu-id="f36db-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f36db-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f36db-127">출력</span><span class="sxs-lookup"><span data-stu-id="f36db-127">OUTPUTS</span></span>

### <span data-ttu-id="f36db-128">PSMediaService (\*).</span><span class="sxs-lookup"><span data-stu-id="f36db-128">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="f36db-129">상속자</span><span class="sxs-lookup"><span data-stu-id="f36db-129">NOTES</span></span>

## <span data-ttu-id="f36db-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f36db-130">RELATED LINKS</span></span>

[<span data-ttu-id="f36db-131">새로운 AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="f36db-131">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="f36db-132">제거-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="f36db-132">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="f36db-133">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="f36db-133">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


