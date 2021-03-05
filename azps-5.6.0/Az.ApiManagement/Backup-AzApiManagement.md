---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 1f0ceb4f349e7fdfee38837561dc436c16cd451b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991783"
---
# <span data-ttu-id="74e17-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74e17-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="74e17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74e17-102">SYNOPSIS</span></span>
<span data-ttu-id="74e17-103">API Management 서비스를 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="74e17-104">구문</span><span class="sxs-lookup"><span data-stu-id="74e17-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74e17-105">설명</span><span class="sxs-lookup"><span data-stu-id="74e17-105">DESCRIPTION</span></span>
<span data-ttu-id="74e17-106">**Backup-AzApiManagement** cmdlet은 Azure API Management 서비스의 인스턴스를 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="74e17-107">이 cmdlet은 백업을 Azure Storage Blob으로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="74e17-108">예제</span><span class="sxs-lookup"><span data-stu-id="74e17-108">EXAMPLES</span></span>

### <span data-ttu-id="74e17-109">예제 1: API Management 서비스 백업</span><span class="sxs-lookup"><span data-stu-id="74e17-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="74e17-110">이 명령은 API Management 서비스를 Storage Blob에 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="74e17-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="74e17-111">PARAMETERS</span></span>

### <span data-ttu-id="74e17-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e17-112">-DefaultProfile</span></span>
<span data-ttu-id="74e17-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74e17-114">-Name</span><span class="sxs-lookup"><span data-stu-id="74e17-114">-Name</span></span>
<span data-ttu-id="74e17-115">이 cmdlet이 백업하는 API Management 배포의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="74e17-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74e17-116">-PassThru</span></span>
<span data-ttu-id="74e17-117">이 cmdlet은 작업이 성공하면 **백업된 PsApiManagement** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="74e17-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e17-118">-ResourceGroupName</span></span>
<span data-ttu-id="74e17-119">API Management 배포가 있는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="74e17-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="74e17-120">-StorageContext</span></span>
<span data-ttu-id="74e17-121">저장소 연결 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="74e17-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="74e17-122">-TargetBlobName</span></span>
<span data-ttu-id="74e17-123">백업에 대한 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="74e17-124">Blob이 없는 경우 이 cmdlet이 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="74e17-125">이 cmdlet은 {Name}-{yyyyy-MM-dd-HH-mm}.apimbackup 패턴에 따라 기본값을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="74e17-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="74e17-126">-TargetContainerName</span></span>
<span data-ttu-id="74e17-127">백업에 대한 Blob의 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="74e17-128">컨테이너가 없는 경우 이 cmdlet이 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="74e17-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e17-129">CommonParameters</span></span>
<span data-ttu-id="74e17-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74e17-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e17-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74e17-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e17-132">입력</span><span class="sxs-lookup"><span data-stu-id="74e17-132">INPUTS</span></span>

### <span data-ttu-id="74e17-133">System.String</span><span class="sxs-lookup"><span data-stu-id="74e17-133">System.String</span></span>

### <span data-ttu-id="74e17-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="74e17-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="74e17-135">출력</span><span class="sxs-lookup"><span data-stu-id="74e17-135">OUTPUTS</span></span>

### <span data-ttu-id="74e17-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="74e17-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="74e17-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74e17-137">NOTES</span></span>

## <span data-ttu-id="74e17-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74e17-138">RELATED LINKS</span></span>

[<span data-ttu-id="74e17-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74e17-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="74e17-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74e17-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="74e17-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74e17-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="74e17-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="74e17-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


