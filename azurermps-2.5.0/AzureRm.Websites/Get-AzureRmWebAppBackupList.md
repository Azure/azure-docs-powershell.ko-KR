---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880846"
---
# <span data-ttu-id="998f3-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="998f3-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="998f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="998f3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="998f3-103">구문과</span><span class="sxs-lookup"><span data-stu-id="998f3-103">SYNTAX</span></span>

### <span data-ttu-id="998f3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="998f3-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="998f3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="998f3-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="998f3-106">설명은</span><span class="sxs-lookup"><span data-stu-id="998f3-106">DESCRIPTION</span></span>
<span data-ttu-id="998f3-107">**AzureRmWebAppBackupList** Cmdlet은 Azure Web App에 대 한 백업 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="998f3-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="998f3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="998f3-108">EXAMPLES</span></span>

### <span data-ttu-id="998f3-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="998f3-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="998f3-110">이 명령은 리소스 그룹 ContosoResourceGroup 연결 된 Web app WebAppStandard와 관련 된 백업 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="998f3-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="998f3-111">변수</span><span class="sxs-lookup"><span data-stu-id="998f3-111">PARAMETERS</span></span>

### <span data-ttu-id="998f3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998f3-112">-DefaultProfile</span></span>
<span data-ttu-id="998f3-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="998f3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="998f3-114">-이름</span><span class="sxs-lookup"><span data-stu-id="998f3-114">-Name</span></span>
<span data-ttu-id="998f3-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="998f3-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998f3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998f3-116">-ResourceGroupName</span></span>
<span data-ttu-id="998f3-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="998f3-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998f3-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="998f3-118">-Slot</span></span>
<span data-ttu-id="998f3-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="998f3-119">Slot name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998f3-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="998f3-120">-WebApp</span></span>
<span data-ttu-id="998f3-121">파이프 Web app</span><span class="sxs-lookup"><span data-stu-id="998f3-121">Piped WebApp</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="998f3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998f3-122">CommonParameters</span></span>
<span data-ttu-id="998f3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="998f3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998f3-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="998f3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998f3-125">입력</span><span class="sxs-lookup"><span data-stu-id="998f3-125">INPUTS</span></span>

### <span data-ttu-id="998f3-126">Site</span><span class="sxs-lookup"><span data-stu-id="998f3-126">Site</span></span>
<span data-ttu-id="998f3-127">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="998f3-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="998f3-128">출력</span><span class="sxs-lookup"><span data-stu-id="998f3-128">OUTPUTS</span></span>

### <span data-ttu-id="998f3-129">Microsoft AzureWebAppBackup []을 (를) 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="998f3-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="998f3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="998f3-130">NOTES</span></span>

## <span data-ttu-id="998f3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="998f3-131">RELATED LINKS</span></span>

