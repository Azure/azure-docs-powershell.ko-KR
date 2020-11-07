---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882086"
---
# <span data-ttu-id="0163e-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0163e-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="0163e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0163e-102">SYNOPSIS</span></span>
<span data-ttu-id="0163e-103">Azure Web App 슬롯을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0163e-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0163e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0163e-104">SYNTAX</span></span>

### <span data-ttu-id="0163e-105">S1</span><span class="sxs-lookup"><span data-stu-id="0163e-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0163e-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="0163e-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0163e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0163e-107">DESCRIPTION</span></span>
<span data-ttu-id="0163e-108">**AzureRmWebAppSlot** Cmdlet은 Azure Web App 슬롯을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0163e-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="0163e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0163e-109">EXAMPLES</span></span>

### <span data-ttu-id="0163e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0163e-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="0163e-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱에 해당 하는 슬롯 Slot001를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="0163e-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0163e-112">변수</span><span class="sxs-lookup"><span data-stu-id="0163e-112">PARAMETERS</span></span>

### <span data-ttu-id="0163e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0163e-113">-DefaultProfile</span></span>
<span data-ttu-id="0163e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0163e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0163e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0163e-115">-Name</span></span>
<span data-ttu-id="0163e-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="0163e-116">WebApp Name</span></span>

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

### <span data-ttu-id="0163e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0163e-117">-ResourceGroupName</span></span>
<span data-ttu-id="0163e-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0163e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0163e-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="0163e-119">-Slot</span></span>
<span data-ttu-id="0163e-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="0163e-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0163e-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="0163e-121">-WebApp</span></span>
<span data-ttu-id="0163e-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="0163e-122">WebApp Object</span></span>

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

### <span data-ttu-id="0163e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0163e-123">CommonParameters</span></span>
<span data-ttu-id="0163e-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0163e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0163e-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0163e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0163e-126">입력</span><span class="sxs-lookup"><span data-stu-id="0163e-126">INPUTS</span></span>

### <span data-ttu-id="0163e-127">Site</span><span class="sxs-lookup"><span data-stu-id="0163e-127">Site</span></span>
<span data-ttu-id="0163e-128">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0163e-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0163e-129">출력</span><span class="sxs-lookup"><span data-stu-id="0163e-129">OUTPUTS</span></span>

## <span data-ttu-id="0163e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0163e-130">NOTES</span></span>

## <span data-ttu-id="0163e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0163e-131">RELATED LINKS</span></span>

