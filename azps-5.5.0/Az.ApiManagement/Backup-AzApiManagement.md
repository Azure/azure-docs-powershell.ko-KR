---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187769"
---
# <span data-ttu-id="39729-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="39729-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="39729-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39729-102">SYNOPSIS</span></span>
<span data-ttu-id="39729-103">API Management 서비스를 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="39729-104">구문</span><span class="sxs-lookup"><span data-stu-id="39729-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39729-105">설명</span><span class="sxs-lookup"><span data-stu-id="39729-105">DESCRIPTION</span></span>
<span data-ttu-id="39729-106">**Backup-AzApiManagement** cmdlet은 Azure API Management 서비스의 인스턴스를 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="39729-107">이 cmdlet은 백업을 Azure Storage Blob으로 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="39729-108">예제</span><span class="sxs-lookup"><span data-stu-id="39729-108">EXAMPLES</span></span>

### <span data-ttu-id="39729-109">예제 1: API Management 서비스 백업</span><span class="sxs-lookup"><span data-stu-id="39729-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="39729-110">이 명령은 API Management 서비스를 Storage Blob에 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="39729-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39729-111">PARAMETERS</span></span>

### <span data-ttu-id="39729-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39729-112">-DefaultProfile</span></span>
<span data-ttu-id="39729-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39729-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39729-114">-Name</span><span class="sxs-lookup"><span data-stu-id="39729-114">-Name</span></span>
<span data-ttu-id="39729-115">이 cmdlet이 백업하는 API Management 배포의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="39729-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39729-116">-PassThru</span></span>
<span data-ttu-id="39729-117">작업이 성공하면 이 cmdlet이 백업된 **PsApiManagement** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="39729-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39729-118">-ResourceGroupName</span></span>
<span data-ttu-id="39729-119">API Management 배포가 있는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="39729-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="39729-120">-StorageContext</span></span>
<span data-ttu-id="39729-121">저장소 연결 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="39729-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="39729-122">-TargetBlobName</span></span>
<span data-ttu-id="39729-123">백업에 대한 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="39729-124">Blob이 없는 경우 이 cmdlet에서 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39729-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="39729-125">이 cmdlet은 {Name}-{yyyy-MM-dd-HH-mm}.apimbackup 패턴에 따라 기본값을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="39729-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="39729-126">-TargetContainerName</span></span>
<span data-ttu-id="39729-127">백업에 대한 Blob 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="39729-128">컨테이너가 없는 경우 이 cmdlet은 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39729-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="39729-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39729-129">CommonParameters</span></span>
<span data-ttu-id="39729-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39729-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39729-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39729-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39729-132">입력</span><span class="sxs-lookup"><span data-stu-id="39729-132">INPUTS</span></span>

### <span data-ttu-id="39729-133">System.String</span><span class="sxs-lookup"><span data-stu-id="39729-133">System.String</span></span>

### <span data-ttu-id="39729-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="39729-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="39729-135">출력</span><span class="sxs-lookup"><span data-stu-id="39729-135">OUTPUTS</span></span>

### <span data-ttu-id="39729-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="39729-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="39729-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39729-137">NOTES</span></span>

## <span data-ttu-id="39729-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39729-138">RELATED LINKS</span></span>

[<span data-ttu-id="39729-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="39729-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="39729-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="39729-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="39729-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="39729-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="39729-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="39729-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


