---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 03c9b54dd83f4689f763ef45e0f9a7c0d8b89672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711465"
---
# <span data-ttu-id="614c4-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="614c4-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="614c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="614c4-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="614c4-103">구문과</span><span class="sxs-lookup"><span data-stu-id="614c4-103">SYNTAX</span></span>

### <span data-ttu-id="614c4-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="614c4-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="614c4-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="614c4-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="614c4-106">설명은</span><span class="sxs-lookup"><span data-stu-id="614c4-106">DESCRIPTION</span></span>
<span data-ttu-id="614c4-107">**AzureRmWebAppBackup** Cmdlet은 Azure Web App 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="614c4-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="614c4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="614c4-108">EXAMPLES</span></span>

### <span data-ttu-id="614c4-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="614c4-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="614c4-110">리소스 그룹 기본값-웹-WestUS에 있는 지정 된 앱 ContosoWebApp의 백업을 만듭니다. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="614c4-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="614c4-111">변수</span><span class="sxs-lookup"><span data-stu-id="614c4-111">PARAMETERS</span></span>

### <span data-ttu-id="614c4-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="614c4-112">-BackupName</span></span>
<span data-ttu-id="614c4-113">백업 이름</span><span class="sxs-lookup"><span data-stu-id="614c4-113">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c4-114">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="614c4-114">-Databases</span></span>
<span data-ttu-id="614c4-115">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="614c4-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c4-116">-이름</span><span class="sxs-lookup"><span data-stu-id="614c4-116">-Name</span></span>
<span data-ttu-id="614c4-117">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="614c4-117">WebApp Name</span></span>

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

### <span data-ttu-id="614c4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="614c4-118">-ResourceGroupName</span></span>
<span data-ttu-id="614c4-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="614c4-119">Resource Group Name</span></span>

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

### <span data-ttu-id="614c4-120">-슬롯</span><span class="sxs-lookup"><span data-stu-id="614c4-120">-Slot</span></span>
<span data-ttu-id="614c4-121">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="614c4-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="614c4-122">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="614c4-122">-StorageAccountUrl</span></span>
<span data-ttu-id="614c4-123">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="614c4-123">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="614c4-124">-Web app</span><span class="sxs-lookup"><span data-stu-id="614c4-124">-WebApp</span></span>
<span data-ttu-id="614c4-125">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="614c4-125">WebApp Object</span></span>

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

### <span data-ttu-id="614c4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614c4-126">-DefaultProfile</span></span>
<span data-ttu-id="614c4-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="614c4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="614c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614c4-128">CommonParameters</span></span>
<span data-ttu-id="614c4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="614c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614c4-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="614c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614c4-131">입력</span><span class="sxs-lookup"><span data-stu-id="614c4-131">INPUTS</span></span>

### <span data-ttu-id="614c4-132">Site</span><span class="sxs-lookup"><span data-stu-id="614c4-132">Site</span></span>
<span data-ttu-id="614c4-133">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="614c4-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="614c4-134">출력</span><span class="sxs-lookup"><span data-stu-id="614c4-134">OUTPUTS</span></span>

### <span data-ttu-id="614c4-135">AzureWebAppBackup (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="614c4-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="614c4-136">상속자</span><span class="sxs-lookup"><span data-stu-id="614c4-136">NOTES</span></span>

## <span data-ttu-id="614c4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="614c4-137">RELATED LINKS</span></span>

