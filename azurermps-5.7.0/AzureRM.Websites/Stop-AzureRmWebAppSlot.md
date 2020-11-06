---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 59fb1d649f5893dc09caa9799cd3412feae06deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526471"
---
# <span data-ttu-id="da070-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="da070-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="da070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da070-102">SYNOPSIS</span></span>
<span data-ttu-id="da070-103">Azure Web App 슬롯을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="da070-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da070-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da070-104">SYNTAX</span></span>

### <span data-ttu-id="da070-105">S1</span><span class="sxs-lookup"><span data-stu-id="da070-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da070-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="da070-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da070-107">설명은</span><span class="sxs-lookup"><span data-stu-id="da070-107">DESCRIPTION</span></span>
<span data-ttu-id="da070-108">**AzureRmWebAppSlot** Cmdlet은 Azure Web App 슬롯을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="da070-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="da070-109">예제의</span><span class="sxs-lookup"><span data-stu-id="da070-109">EXAMPLES</span></span>

### <span data-ttu-id="da070-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="da070-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="da070-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱에 해당 하는 슬롯 Slot001를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="da070-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="da070-112">변수</span><span class="sxs-lookup"><span data-stu-id="da070-112">PARAMETERS</span></span>

### <span data-ttu-id="da070-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da070-113">-DefaultProfile</span></span>
<span data-ttu-id="da070-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da070-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da070-115">-이름</span><span class="sxs-lookup"><span data-stu-id="da070-115">-Name</span></span>
<span data-ttu-id="da070-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="da070-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da070-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da070-117">-ResourceGroupName</span></span>
<span data-ttu-id="da070-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="da070-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da070-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="da070-119">-Slot</span></span>
<span data-ttu-id="da070-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="da070-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da070-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="da070-121">-WebApp</span></span>
<span data-ttu-id="da070-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="da070-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da070-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da070-123">CommonParameters</span></span>
<span data-ttu-id="da070-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da070-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da070-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da070-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da070-126">입력</span><span class="sxs-lookup"><span data-stu-id="da070-126">INPUTS</span></span>

### <span data-ttu-id="da070-127">Site</span><span class="sxs-lookup"><span data-stu-id="da070-127">Site</span></span>
<span data-ttu-id="da070-128">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da070-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="da070-129">출력</span><span class="sxs-lookup"><span data-stu-id="da070-129">OUTPUTS</span></span>

## <span data-ttu-id="da070-130">상속자</span><span class="sxs-lookup"><span data-stu-id="da070-130">NOTES</span></span>

## <span data-ttu-id="da070-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da070-131">RELATED LINKS</span></span>

