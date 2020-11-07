---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 4ac4482cb5972553b1dad3972200d2f0eb032fe4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876086"
---
# <span data-ttu-id="d7764-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d7764-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="d7764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7764-102">SYNOPSIS</span></span>
<span data-ttu-id="d7764-103">Azure Web App 슬롯을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7764-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="d7764-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7764-104">SYNTAX</span></span>

### <span data-ttu-id="d7764-105">S1</span><span class="sxs-lookup"><span data-stu-id="d7764-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7764-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="d7764-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7764-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d7764-107">DESCRIPTION</span></span>
<span data-ttu-id="d7764-108">**AzWebAppSlot** Cmdlet은 Azure Web App 슬롯을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7764-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="d7764-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d7764-109">EXAMPLES</span></span>

### <span data-ttu-id="d7764-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7764-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d7764-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱에 해당 하는 슬롯 Slot001를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7764-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d7764-112">변수</span><span class="sxs-lookup"><span data-stu-id="d7764-112">PARAMETERS</span></span>

### <span data-ttu-id="d7764-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7764-113">-DefaultProfile</span></span>
<span data-ttu-id="d7764-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7764-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7764-115">-이름</span><span class="sxs-lookup"><span data-stu-id="d7764-115">-Name</span></span>
<span data-ttu-id="d7764-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="d7764-116">WebApp Name</span></span>

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

### <span data-ttu-id="d7764-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7764-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7764-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d7764-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d7764-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="d7764-119">-Slot</span></span>
<span data-ttu-id="d7764-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="d7764-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d7764-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="d7764-121">-WebApp</span></span>
<span data-ttu-id="d7764-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="d7764-122">WebApp Object</span></span>

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

### <span data-ttu-id="d7764-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7764-123">CommonParameters</span></span>
<span data-ttu-id="d7764-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7764-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7764-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7764-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7764-126">입력</span><span class="sxs-lookup"><span data-stu-id="d7764-126">INPUTS</span></span>

### <span data-ttu-id="d7764-127">Site</span><span class="sxs-lookup"><span data-stu-id="d7764-127">Site</span></span>
<span data-ttu-id="d7764-128">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7764-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d7764-129">출력</span><span class="sxs-lookup"><span data-stu-id="d7764-129">OUTPUTS</span></span>

## <span data-ttu-id="d7764-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d7764-130">NOTES</span></span>

## <span data-ttu-id="d7764-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7764-131">RELATED LINKS</span></span>

