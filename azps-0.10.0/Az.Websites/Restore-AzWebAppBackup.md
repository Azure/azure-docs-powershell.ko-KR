---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: f93a173e79cb34c5603ce58fc3e03c92869a5d01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876104"
---
# <span data-ttu-id="ef2d2-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ef2d2-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="ef2d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef2d2-102">SYNOPSIS</span></span>

## <span data-ttu-id="ef2d2-103">구문과</span><span class="sxs-lookup"><span data-stu-id="ef2d2-103">SYNTAX</span></span>

### <span data-ttu-id="ef2d2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ef2d2-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="ef2d2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ef2d2-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="ef2d2-106">설명은</span><span class="sxs-lookup"><span data-stu-id="ef2d2-106">DESCRIPTION</span></span>
<span data-ttu-id="ef2d2-107">**Restore-AzWebAppBackup** Cmdlet은 Azure Web App 백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2d2-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="ef2d2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ef2d2-108">EXAMPLES</span></span>

### <span data-ttu-id="ef2d2-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="ef2d2-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="ef2d2-110">리소스 그룹 Default-WestUS 내에 있는 지정 된 앱 ContosoWebApp의 백업을 다음 위치의 blob "myBlob"에 복원 합니다. https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="ef2d2-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="ef2d2-111">변수</span><span class="sxs-lookup"><span data-stu-id="ef2d2-111">PARAMETERS</span></span>

### <span data-ttu-id="ef2d2-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ef2d2-112">-AppServicePlan</span></span>
<span data-ttu-id="ef2d2-113">복원 된 앱에 대 한 앱 서비스 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2d2-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="ef2d2-114">이 옵션을 비워 두면 앱의 현재 앱 서비스 계획이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef2d2-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef2d2-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="ef2d2-115">-BlobName</span></span>
<span data-ttu-id="ef2d2-116">Blob 이름</span><span class="sxs-lookup"><span data-stu-id="ef2d2-116">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef2d2-117">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="ef2d2-117">-Databases</span></span>
<span data-ttu-id="ef2d2-118">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="ef2d2-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ef2d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef2d2-119">-DefaultProfile</span></span>
<span data-ttu-id="ef2d2-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef2d2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef2d2-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="ef2d2-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="ef2d2-122">충돌 하는 호스트 이름 무시 옵션</span><span class="sxs-lookup"><span data-stu-id="ef2d2-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef2d2-123">-이름</span><span class="sxs-lookup"><span data-stu-id="ef2d2-123">-Name</span></span>
<span data-ttu-id="ef2d2-124">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="ef2d2-124">WebApp Name</span></span>

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

### <span data-ttu-id="ef2d2-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ef2d2-125">-Overwrite</span></span>
<span data-ttu-id="ef2d2-126">덮어쓰기 옵션</span><span class="sxs-lookup"><span data-stu-id="ef2d2-126">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef2d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef2d2-127">-ResourceGroupName</span></span>
<span data-ttu-id="ef2d2-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ef2d2-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ef2d2-129">-슬롯</span><span class="sxs-lookup"><span data-stu-id="ef2d2-129">-Slot</span></span>
<span data-ttu-id="ef2d2-130">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="ef2d2-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ef2d2-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ef2d2-131">-StorageAccountUrl</span></span>
<span data-ttu-id="ef2d2-132">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="ef2d2-132">Storage Account Url</span></span>

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

### <span data-ttu-id="ef2d2-133">-Web app</span><span class="sxs-lookup"><span data-stu-id="ef2d2-133">-WebApp</span></span>
<span data-ttu-id="ef2d2-134">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="ef2d2-134">WebApp Object</span></span>

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

### <span data-ttu-id="ef2d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef2d2-135">CommonParameters</span></span>
<span data-ttu-id="ef2d2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef2d2-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef2d2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef2d2-138">입력</span><span class="sxs-lookup"><span data-stu-id="ef2d2-138">INPUTS</span></span>

### <span data-ttu-id="ef2d2-139">Site</span><span class="sxs-lookup"><span data-stu-id="ef2d2-139">Site</span></span>
<span data-ttu-id="ef2d2-140">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef2d2-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ef2d2-141">출력</span><span class="sxs-lookup"><span data-stu-id="ef2d2-141">OUTPUTS</span></span>

## <span data-ttu-id="ef2d2-142">상속자</span><span class="sxs-lookup"><span data-stu-id="ef2d2-142">NOTES</span></span>

## <span data-ttu-id="ef2d2-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef2d2-143">RELATED LINKS</span></span>

