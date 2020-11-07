---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 7245697cab6184aa5fc2f7c292875f96cf3de3fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881201"
---
# <span data-ttu-id="eeab7-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="eeab7-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="eeab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeab7-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeab7-103">구문과</span><span class="sxs-lookup"><span data-stu-id="eeab7-103">SYNTAX</span></span>

### <span data-ttu-id="eeab7-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="eeab7-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="eeab7-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="eeab7-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="eeab7-106">설명은</span><span class="sxs-lookup"><span data-stu-id="eeab7-106">DESCRIPTION</span></span>
<span data-ttu-id="eeab7-107">**AzureRmWebAppBackup** Cmdlet은 Azure Web App 백업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eeab7-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="eeab7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="eeab7-108">EXAMPLES</span></span>

### <span data-ttu-id="eeab7-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="eeab7-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="eeab7-110">리소스 그룹 기본값-웹-WestUS에 있는 지정 된 앱 ContosoWebApp의 백업을 만듭니다. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="eeab7-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="eeab7-111">변수</span><span class="sxs-lookup"><span data-stu-id="eeab7-111">PARAMETERS</span></span>

### <span data-ttu-id="eeab7-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="eeab7-112">-BackupName</span></span>
<span data-ttu-id="eeab7-113">백업 이름</span><span class="sxs-lookup"><span data-stu-id="eeab7-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeab7-114">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="eeab7-114">-Databases</span></span>
<span data-ttu-id="eeab7-115">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="eeab7-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeab7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeab7-116">-DefaultProfile</span></span>
<span data-ttu-id="eeab7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eeab7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeab7-118">-이름</span><span class="sxs-lookup"><span data-stu-id="eeab7-118">-Name</span></span>
<span data-ttu-id="eeab7-119">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="eeab7-119">WebApp Name</span></span>

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

### <span data-ttu-id="eeab7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeab7-120">-ResourceGroupName</span></span>
<span data-ttu-id="eeab7-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="eeab7-121">Resource Group Name</span></span>

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

### <span data-ttu-id="eeab7-122">-슬롯</span><span class="sxs-lookup"><span data-stu-id="eeab7-122">-Slot</span></span>
<span data-ttu-id="eeab7-123">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="eeab7-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="eeab7-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="eeab7-124">-StorageAccountUrl</span></span>
<span data-ttu-id="eeab7-125">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="eeab7-125">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeab7-126">-Web app</span><span class="sxs-lookup"><span data-stu-id="eeab7-126">-WebApp</span></span>
<span data-ttu-id="eeab7-127">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="eeab7-127">WebApp Object</span></span>

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

### <span data-ttu-id="eeab7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeab7-128">CommonParameters</span></span>
<span data-ttu-id="eeab7-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeab7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeab7-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeab7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeab7-131">입력</span><span class="sxs-lookup"><span data-stu-id="eeab7-131">INPUTS</span></span>

### <span data-ttu-id="eeab7-132">Site</span><span class="sxs-lookup"><span data-stu-id="eeab7-132">Site</span></span>
<span data-ttu-id="eeab7-133">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeab7-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="eeab7-134">출력</span><span class="sxs-lookup"><span data-stu-id="eeab7-134">OUTPUTS</span></span>

### <span data-ttu-id="eeab7-135">AzureWebAppBackup (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="eeab7-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="eeab7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="eeab7-136">NOTES</span></span>

## <span data-ttu-id="eeab7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eeab7-137">RELATED LINKS</span></span>

