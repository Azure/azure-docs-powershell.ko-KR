---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218887"
---
# <span data-ttu-id="f4898-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="f4898-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="f4898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4898-102">SYNOPSIS</span></span>
<span data-ttu-id="f4898-103">미디어 서비스와 연결 된 REST 끝점에 액세스 하는 데 필요한 키 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4898-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="f4898-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4898-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4898-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f4898-105">DESCRIPTION</span></span>
<span data-ttu-id="f4898-106">**AzMediaServiceKey** Cmdlet은 Azure 미디어 서비스와 연결 된 REST (Representational State Transfer) 끝점에 액세스 하는 데 필요한 주요 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4898-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="f4898-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f4898-107">EXAMPLES</span></span>

### <span data-ttu-id="f4898-108">예제 1: 미디어 서비스에 액세스 하는 데 필요한 주요 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="f4898-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="f4898-109">이 명령은 ResourceGroup001 이라는 리소스 그룹에 속하는 MediaService001 이라는 미디어 서비스에 액세스 하기 위한 키 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f4898-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="f4898-110">변수</span><span class="sxs-lookup"><span data-stu-id="f4898-110">PARAMETERS</span></span>

### <span data-ttu-id="f4898-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4898-111">-AccountName</span></span>
<span data-ttu-id="f4898-112">이 cmdlet이 미디어 서비스 키를 가져오는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4898-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="f4898-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4898-113">-DefaultProfile</span></span>
<span data-ttu-id="f4898-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f4898-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4898-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4898-115">-ResourceGroupName</span></span>
<span data-ttu-id="f4898-116">미디어 서비스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4898-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f4898-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4898-117">CommonParameters</span></span>
<span data-ttu-id="f4898-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4898-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4898-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4898-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4898-120">입력</span><span class="sxs-lookup"><span data-stu-id="f4898-120">INPUTS</span></span>

### <span data-ttu-id="f4898-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f4898-121">System.String</span></span>

## <span data-ttu-id="f4898-122">출력</span><span class="sxs-lookup"><span data-stu-id="f4898-122">OUTPUTS</span></span>

### <span data-ttu-id="f4898-123">Microsoft. w i m.</span><span class="sxs-lookup"><span data-stu-id="f4898-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="f4898-124">상속자</span><span class="sxs-lookup"><span data-stu-id="f4898-124">NOTES</span></span>

## <span data-ttu-id="f4898-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4898-125">RELATED LINKS</span></span>

[<span data-ttu-id="f4898-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="f4898-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


