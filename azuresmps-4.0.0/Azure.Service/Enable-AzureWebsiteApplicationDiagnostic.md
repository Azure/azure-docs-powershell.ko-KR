---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045682"
---
# <span data-ttu-id="0b71f-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0b71f-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="0b71f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b71f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b71f-103">Azure 웹 사이트에서 응용 프로그램 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="0b71f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b71f-104">SYNTAX</span></span>

### <span data-ttu-id="0b71f-105">FileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b71f-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0b71f-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b71f-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0b71f-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b71f-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0b71f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0b71f-108">DESCRIPTION</span></span>
<span data-ttu-id="0b71f-109">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0b71f-110">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0b71f-111">Azure 웹 사이트에서 응용 프로그램 진단을 사용 하도록 설정 하 고, 파일 시스템 또는 Azure storage에서 로그 저장소를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="0b71f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0b71f-112">EXAMPLES</span></span>

### <span data-ttu-id="0b71f-113">예제 1: 파일 시스템을 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="0b71f-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="0b71f-114">이 예제에서는 세부 정보 표시 수준이 있는 파일 시스템에서 응용 프로그램 로깅을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="0b71f-115">예제 2: Azure Storage를 사용 하 여 로깅 사용</span><span class="sxs-lookup"><span data-stu-id="0b71f-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="0b71f-116">이 예제에서는 로깅 수준이 정보로 설정 된 내 계정 이라는 저장소 계정을 사용 하 여 응용 프로그램을 로깅할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="0b71f-117">변수</span><span class="sxs-lookup"><span data-stu-id="0b71f-117">PARAMETERS</span></span>

### <span data-ttu-id="0b71f-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="0b71f-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-119">-파일</span><span class="sxs-lookup"><span data-stu-id="0b71f-119">-File</span></span>
<span data-ttu-id="0b71f-120">파일 시스템을 사용 하 여 로그 파일을 저장할 것인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="0b71f-121">-LogLevel</span></span>
<span data-ttu-id="0b71f-122">저장할 로그 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-122">The log level to store.</span></span>
<span data-ttu-id="0b71f-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b71f-124">오류</span><span class="sxs-lookup"><span data-stu-id="0b71f-124">Error</span></span>
- <span data-ttu-id="0b71f-125">오류</span><span class="sxs-lookup"><span data-stu-id="0b71f-125">Warning</span></span>
- <span data-ttu-id="0b71f-126">방법</span><span class="sxs-lookup"><span data-stu-id="0b71f-126">Information</span></span>
- <span data-ttu-id="0b71f-127">정보</span><span class="sxs-lookup"><span data-stu-id="0b71f-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-128">-이름</span><span class="sxs-lookup"><span data-stu-id="0b71f-128">-Name</span></span>
<span data-ttu-id="0b71f-129">Azure 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-129">Specifies the name of the Azure website.</span></span>

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

### <span data-ttu-id="0b71f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b71f-130">-PassThru</span></span>
<span data-ttu-id="0b71f-131">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b71f-132">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-132">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="0b71f-133">-Profile</span></span>
<span data-ttu-id="0b71f-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b71f-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-136">-슬롯</span><span class="sxs-lookup"><span data-stu-id="0b71f-136">-Slot</span></span>
<span data-ttu-id="0b71f-137">슬롯의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-137">Specifies the name of the slot.</span></span>

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

### <span data-ttu-id="0b71f-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0b71f-138">-StorageAccountName</span></span>
<span data-ttu-id="0b71f-139">로그를 저장 하는 데 사용할 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="0b71f-140">지정 하지 않으면 CurrentStorageAccount를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="0b71f-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="0b71f-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="0b71f-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b71f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b71f-144">CommonParameters</span></span>
<span data-ttu-id="0b71f-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b71f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b71f-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b71f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b71f-147">입력</span><span class="sxs-lookup"><span data-stu-id="0b71f-147">INPUTS</span></span>

## <span data-ttu-id="0b71f-148">출력</span><span class="sxs-lookup"><span data-stu-id="0b71f-148">OUTPUTS</span></span>

## <span data-ttu-id="0b71f-149">상속자</span><span class="sxs-lookup"><span data-stu-id="0b71f-149">NOTES</span></span>

## <span data-ttu-id="0b71f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b71f-150">RELATED LINKS</span></span>

[<span data-ttu-id="0b71f-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0b71f-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="0b71f-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b71f-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="0b71f-153">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b71f-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="0b71f-154">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b71f-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="0b71f-155">시작-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0b71f-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


