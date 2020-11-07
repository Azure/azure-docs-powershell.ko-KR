---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 104614bd0fdd2ca8555765a301f6b257cdac0bc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877981"
---
# <span data-ttu-id="c381e-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="c381e-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="c381e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c381e-102">SYNOPSIS</span></span>

## <span data-ttu-id="c381e-103">구문과</span><span class="sxs-lookup"><span data-stu-id="c381e-103">SYNTAX</span></span>

### <span data-ttu-id="c381e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c381e-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c381e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c381e-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c381e-106">설명은</span><span class="sxs-lookup"><span data-stu-id="c381e-106">DESCRIPTION</span></span>
<span data-ttu-id="c381e-107">**AzWebAppBackupList** Cmdlet은 Azure Web App에 대 한 백업 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c381e-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="c381e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c381e-108">EXAMPLES</span></span>

### <span data-ttu-id="c381e-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="c381e-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="c381e-110">이 명령은 리소스 그룹 ContosoResourceGroup 연결 된 Web app WebAppStandard와 관련 된 백업 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c381e-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="c381e-111">변수</span><span class="sxs-lookup"><span data-stu-id="c381e-111">PARAMETERS</span></span>

### <span data-ttu-id="c381e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c381e-112">-DefaultProfile</span></span>
<span data-ttu-id="c381e-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c381e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c381e-114">-이름</span><span class="sxs-lookup"><span data-stu-id="c381e-114">-Name</span></span>
<span data-ttu-id="c381e-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="c381e-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c381e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c381e-116">-ResourceGroupName</span></span>
<span data-ttu-id="c381e-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c381e-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c381e-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="c381e-118">-Slot</span></span>
<span data-ttu-id="c381e-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="c381e-119">Slot name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c381e-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="c381e-120">-WebApp</span></span>
<span data-ttu-id="c381e-121">파이프 Web app</span><span class="sxs-lookup"><span data-stu-id="c381e-121">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c381e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c381e-122">CommonParameters</span></span>
<span data-ttu-id="c381e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c381e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c381e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c381e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c381e-125">입력</span><span class="sxs-lookup"><span data-stu-id="c381e-125">INPUTS</span></span>

### <span data-ttu-id="c381e-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c381e-126">System.String</span></span>

### <span data-ttu-id="c381e-127">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="c381e-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c381e-128">출력</span><span class="sxs-lookup"><span data-stu-id="c381e-128">OUTPUTS</span></span>

### <span data-ttu-id="c381e-129">AzureWebAppBackup (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="c381e-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="c381e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c381e-130">NOTES</span></span>

## <span data-ttu-id="c381e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c381e-131">RELATED LINKS</span></span>
