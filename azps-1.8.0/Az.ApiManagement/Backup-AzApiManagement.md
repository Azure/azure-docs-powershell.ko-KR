---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 576c623b942ec496d2800c1ad5432f72eb6911bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689167"
---
# <span data-ttu-id="fbeff-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbeff-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="fbeff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbeff-102">SYNOPSIS</span></span>
<span data-ttu-id="fbeff-103">API Management 서비스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="fbeff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fbeff-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbeff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fbeff-105">DESCRIPTION</span></span>
<span data-ttu-id="fbeff-106">**AzApiManagement** Cmdlet은 Azure API Management 서비스의 인스턴스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="fbeff-107">이 cmdlet은 백업을 Azure Storage blob로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="fbeff-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fbeff-108">EXAMPLES</span></span>

### <span data-ttu-id="fbeff-109">예제 1: API Management 서비스 백업</span><span class="sxs-lookup"><span data-stu-id="fbeff-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="fbeff-110">이 명령은 저장소 blob에 API Management 서비스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="fbeff-111">변수</span><span class="sxs-lookup"><span data-stu-id="fbeff-111">PARAMETERS</span></span>

### <span data-ttu-id="fbeff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbeff-112">-DefaultProfile</span></span>
<span data-ttu-id="fbeff-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbeff-114">-이름</span><span class="sxs-lookup"><span data-stu-id="fbeff-114">-Name</span></span>
<span data-ttu-id="fbeff-115">이 cmdlet이 백업 하는 API 관리 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbeff-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbeff-116">-PassThru</span></span>
<span data-ttu-id="fbeff-117">작업이 성공한 경우이 cmdlet이 백업 된 **PsApiManagement** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbeff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbeff-118">-ResourceGroupName</span></span>
<span data-ttu-id="fbeff-119">API Management 배포가 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbeff-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="fbeff-120">-StorageContext</span></span>
<span data-ttu-id="fbeff-121">저장소 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbeff-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="fbeff-122">-TargetBlobName</span></span>
<span data-ttu-id="fbeff-123">백업에 대 한 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="fbeff-124">Blob이 없는 경우이 cmdlet은이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="fbeff-125">이 cmdlet은 {Name}-{yyyy-MM-dd-HH-mm}.</span><span class="sxs-lookup"><span data-stu-id="fbeff-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbeff-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="fbeff-126">-TargetContainerName</span></span>
<span data-ttu-id="fbeff-127">백업용 blob 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="fbeff-128">컨테이너가 없으면이 cmdlet에서 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-128">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbeff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbeff-129">CommonParameters</span></span>
<span data-ttu-id="fbeff-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbeff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbeff-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbeff-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbeff-132">입력</span><span class="sxs-lookup"><span data-stu-id="fbeff-132">INPUTS</span></span>

### <span data-ttu-id="fbeff-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fbeff-133">System.String</span></span>

### <span data-ttu-id="fbeff-134">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fbeff-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fbeff-135">출력</span><span class="sxs-lookup"><span data-stu-id="fbeff-135">OUTPUTS</span></span>

### <span data-ttu-id="fbeff-136">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="fbeff-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="fbeff-137">상속자</span><span class="sxs-lookup"><span data-stu-id="fbeff-137">NOTES</span></span>

## <span data-ttu-id="fbeff-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbeff-138">RELATED LINKS</span></span>

[<span data-ttu-id="fbeff-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbeff-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="fbeff-140">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbeff-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="fbeff-141">제거-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbeff-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="fbeff-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="fbeff-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


