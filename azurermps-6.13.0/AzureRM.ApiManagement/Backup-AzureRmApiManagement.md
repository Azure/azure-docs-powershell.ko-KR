---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d8f243b0b02d724a3979b8c8f318be8e58623cf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533491"
---
# <span data-ttu-id="11d28-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d28-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="11d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11d28-102">SYNOPSIS</span></span>
<span data-ttu-id="11d28-103">API Management 서비스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11d28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11d28-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11d28-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11d28-105">DESCRIPTION</span></span>
<span data-ttu-id="11d28-106">**AzureRmApiManagement** Cmdlet은 Azure API Management 서비스의 인스턴스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="11d28-107">이 cmdlet은 백업을 Azure Storage blob로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="11d28-108">예제의</span><span class="sxs-lookup"><span data-stu-id="11d28-108">EXAMPLES</span></span>

### <span data-ttu-id="11d28-109">예제 1: API Management 서비스 백업</span><span class="sxs-lookup"><span data-stu-id="11d28-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="11d28-110">이 명령은 저장소 blob에 API Management 서비스를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="11d28-111">변수</span><span class="sxs-lookup"><span data-stu-id="11d28-111">PARAMETERS</span></span>

### <span data-ttu-id="11d28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d28-112">-DefaultProfile</span></span>
<span data-ttu-id="11d28-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11d28-114">-이름</span><span class="sxs-lookup"><span data-stu-id="11d28-114">-Name</span></span>
<span data-ttu-id="11d28-115">이 cmdlet이 백업 하는 API 관리 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="11d28-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11d28-116">-PassThru</span></span>
<span data-ttu-id="11d28-117">작업이 성공한 경우이 cmdlet이 백업 된 **PsApiManagement** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="11d28-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d28-118">-ResourceGroupName</span></span>
<span data-ttu-id="11d28-119">API Management 배포가 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="11d28-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="11d28-120">-StorageContext</span></span>
<span data-ttu-id="11d28-121">저장소 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="11d28-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="11d28-122">-TargetBlobName</span></span>
<span data-ttu-id="11d28-123">백업에 대 한 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="11d28-124">Blob이 없는 경우이 cmdlet은이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="11d28-125">이 cmdlet은 {Name}-{yyyy-MM-dd-HH-mm}.</span><span class="sxs-lookup"><span data-stu-id="11d28-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="11d28-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="11d28-126">-TargetContainerName</span></span>
<span data-ttu-id="11d28-127">백업용 blob 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="11d28-128">컨테이너가 없으면이 cmdlet에서 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="11d28-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d28-129">CommonParameters</span></span>
<span data-ttu-id="11d28-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11d28-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d28-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11d28-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d28-132">입력</span><span class="sxs-lookup"><span data-stu-id="11d28-132">INPUTS</span></span>

### <span data-ttu-id="11d28-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11d28-133">System.String</span></span>

### <span data-ttu-id="11d28-134">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="11d28-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="11d28-135">출력</span><span class="sxs-lookup"><span data-stu-id="11d28-135">OUTPUTS</span></span>

### <span data-ttu-id="11d28-136">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="11d28-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="11d28-137">상속자</span><span class="sxs-lookup"><span data-stu-id="11d28-137">NOTES</span></span>

## <span data-ttu-id="11d28-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11d28-138">RELATED LINKS</span></span>

[<span data-ttu-id="11d28-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d28-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="11d28-140">새로운 AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d28-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="11d28-141">제거-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d28-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="11d28-142">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="11d28-142">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


