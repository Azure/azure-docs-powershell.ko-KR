---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 9c23484fa5f8b45548985645db45872fcc63f66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533536"
---
# <span data-ttu-id="6e3d1-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e3d1-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="6e3d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e3d1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e3d1-103">구문과</span><span class="sxs-lookup"><span data-stu-id="6e3d1-103">SYNTAX</span></span>

### <span data-ttu-id="6e3d1-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6e3d1-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="6e3d1-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6e3d1-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="6e3d1-106">설명은</span><span class="sxs-lookup"><span data-stu-id="6e3d1-106">DESCRIPTION</span></span>
<span data-ttu-id="6e3d1-107">**편집-AzureRmWebAppBackupConfiguration** Cmdlet은 Azure Web App에 대 한 현재 구성 백업을 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3d1-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="6e3d1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6e3d1-108">EXAMPLES</span></span>

## <span data-ttu-id="6e3d1-109">변수</span><span class="sxs-lookup"><span data-stu-id="6e3d1-109">PARAMETERS</span></span>

### <span data-ttu-id="6e3d1-110">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="6e3d1-110">-Databases</span></span>
<span data-ttu-id="6e3d1-111">DatabaseBackupSetting 유형의 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="6e3d1-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3d1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3d1-112">-DefaultProfile</span></span>
<span data-ttu-id="6e3d1-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3d1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e3d1-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="6e3d1-114">-FrequencyInterval</span></span>
<span data-ttu-id="6e3d1-115">빈도 간격</span><span class="sxs-lookup"><span data-stu-id="6e3d1-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3d1-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="6e3d1-116">-FrequencyUnit</span></span>
<span data-ttu-id="6e3d1-117">주파수 단위</span><span class="sxs-lookup"><span data-stu-id="6e3d1-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3d1-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="6e3d1-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="6e3d1-119">하나 이상의 백업 옵션 유지</span><span class="sxs-lookup"><span data-stu-id="6e3d1-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3d1-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6e3d1-120">-Name</span></span>
<span data-ttu-id="6e3d1-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="6e3d1-121">WebApp Name</span></span>

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

### <span data-ttu-id="6e3d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e3d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="6e3d1-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6e3d1-123">Resource Group Name</span></span>

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

### <span data-ttu-id="6e3d1-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="6e3d1-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="6e3d1-125">보존 기간 (일)</span><span class="sxs-lookup"><span data-stu-id="6e3d1-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3d1-126">-슬롯</span><span class="sxs-lookup"><span data-stu-id="6e3d1-126">-Slot</span></span>
<span data-ttu-id="6e3d1-127">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="6e3d1-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6e3d1-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6e3d1-128">-StartTime</span></span>
<span data-ttu-id="6e3d1-129">UTC의 StartTime</span><span class="sxs-lookup"><span data-stu-id="6e3d1-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3d1-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="6e3d1-130">-StorageAccountUrl</span></span>
<span data-ttu-id="6e3d1-131">저장소 계정 Url</span><span class="sxs-lookup"><span data-stu-id="6e3d1-131">Storage Account Url</span></span>

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

### <span data-ttu-id="6e3d1-132">-Web app</span><span class="sxs-lookup"><span data-stu-id="6e3d1-132">-WebApp</span></span>
<span data-ttu-id="6e3d1-133">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="6e3d1-133">WebApp Object</span></span>

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

### <span data-ttu-id="6e3d1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3d1-134">CommonParameters</span></span>
<span data-ttu-id="6e3d1-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3d1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3d1-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e3d1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3d1-137">입력</span><span class="sxs-lookup"><span data-stu-id="6e3d1-137">INPUTS</span></span>

### <span data-ttu-id="6e3d1-138">Site</span><span class="sxs-lookup"><span data-stu-id="6e3d1-138">Site</span></span>
<span data-ttu-id="6e3d1-139">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3d1-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6e3d1-140">출력</span><span class="sxs-lookup"><span data-stu-id="6e3d1-140">OUTPUTS</span></span>

### <span data-ttu-id="6e3d1-141">AzureWebAppBackupConfiguration (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="6e3d1-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="6e3d1-142">상속자</span><span class="sxs-lookup"><span data-stu-id="6e3d1-142">NOTES</span></span>

## <span data-ttu-id="6e3d1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e3d1-143">RELATED LINKS</span></span>

[<span data-ttu-id="6e3d1-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e3d1-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


