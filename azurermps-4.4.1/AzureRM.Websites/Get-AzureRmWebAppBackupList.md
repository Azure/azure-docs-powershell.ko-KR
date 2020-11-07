---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: 02c83e79b5f56d4ef9a6d7730efb5cf5c42a9da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703071"
---
# <span data-ttu-id="24c1a-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="24c1a-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="24c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c1a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24c1a-103">구문과</span><span class="sxs-lookup"><span data-stu-id="24c1a-103">SYNTAX</span></span>

### <span data-ttu-id="24c1a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="24c1a-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24c1a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="24c1a-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24c1a-106">설명은</span><span class="sxs-lookup"><span data-stu-id="24c1a-106">DESCRIPTION</span></span>
<span data-ttu-id="24c1a-107">**AzureRmWebAppBackupList** Cmdlet은 Azure Web App에 대 한 백업 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24c1a-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="24c1a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="24c1a-108">EXAMPLES</span></span>

### <span data-ttu-id="24c1a-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="24c1a-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="24c1a-110">이 명령은 리소스 그룹 ContosoResourceGroup 연결 된 Web app WebAppStandard와 관련 된 백업 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c1a-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="24c1a-111">변수</span><span class="sxs-lookup"><span data-stu-id="24c1a-111">PARAMETERS</span></span>

### <span data-ttu-id="24c1a-112">-이름</span><span class="sxs-lookup"><span data-stu-id="24c1a-112">-Name</span></span>
<span data-ttu-id="24c1a-113">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="24c1a-113">WebApp Name</span></span>

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

### <span data-ttu-id="24c1a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c1a-114">-ResourceGroupName</span></span>
<span data-ttu-id="24c1a-115">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="24c1a-115">Resource Group Name</span></span>

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

### <span data-ttu-id="24c1a-116">-슬롯</span><span class="sxs-lookup"><span data-stu-id="24c1a-116">-Slot</span></span>
<span data-ttu-id="24c1a-117">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="24c1a-117">Slot name</span></span>

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

### <span data-ttu-id="24c1a-118">-Web app</span><span class="sxs-lookup"><span data-stu-id="24c1a-118">-WebApp</span></span>
<span data-ttu-id="24c1a-119">파이프 Web app</span><span class="sxs-lookup"><span data-stu-id="24c1a-119">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24c1a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c1a-120">-DefaultProfile</span></span>
<span data-ttu-id="24c1a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24c1a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c1a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c1a-122">CommonParameters</span></span>
<span data-ttu-id="24c1a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c1a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c1a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c1a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c1a-125">입력</span><span class="sxs-lookup"><span data-stu-id="24c1a-125">INPUTS</span></span>

### <span data-ttu-id="24c1a-126">Site</span><span class="sxs-lookup"><span data-stu-id="24c1a-126">Site</span></span>
<span data-ttu-id="24c1a-127">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c1a-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="24c1a-128">출력</span><span class="sxs-lookup"><span data-stu-id="24c1a-128">OUTPUTS</span></span>

### <span data-ttu-id="24c1a-129">Microsoft AzureWebAppBackup []을 (를) 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="24c1a-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="24c1a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="24c1a-130">NOTES</span></span>

## <span data-ttu-id="24c1a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24c1a-131">RELATED LINKS</span></span>

