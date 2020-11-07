---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702492"
---
# <span data-ttu-id="06975-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="06975-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="06975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06975-102">SYNOPSIS</span></span>
<span data-ttu-id="06975-103">백업 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06975-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06975-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06975-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06975-105">설명은</span><span class="sxs-lookup"><span data-stu-id="06975-105">DESCRIPTION</span></span>
<span data-ttu-id="06975-106">**Get-AzureRmBackupContainer** Cmdlet은 Azure 백업 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06975-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>
<span data-ttu-id="06975-107">**Azurebackupcontainer** 는 데이터 원본, 보호 된 항목 및 복구 지점을 캡슐화 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="06975-108">**Azurebackupcontainer** 는 다음 중 하나가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06975-108">An **AzureBackupContainer** can be one of the following:</span></span> 
- <span data-ttu-id="06975-109">Windows Server 컴퓨터</span><span class="sxs-lookup"><span data-stu-id="06975-109">A Windows Server computer</span></span>
- <span data-ttu-id="06975-110">SCDPM (System Center Data Protection Manager) 서버</span><span class="sxs-lookup"><span data-stu-id="06975-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="06975-111">Azure 인프라 (IaaS) 가상 컴퓨터 백업 하기 전에 데이터 원본 또는 항목을 백업할 수 있으려면 Azure Backup service를 사용 하 여 컨테이너를 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-111">An Azure infrastructure as a service (IaaS) virtual machine Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="06975-112">백업 자격 증명 모음에 백업 데이터를 보내려면 컨테이너를 인증 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-112">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="06975-113">Windows Server 컴퓨터 및 SCDPM 서버의 경우 등록은 서버의 정규화 된 도메인 이름과 함께 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06975-113">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="06975-114">예제의</span><span class="sxs-lookup"><span data-stu-id="06975-114">EXAMPLES</span></span>

### <span data-ttu-id="06975-115">예제 1: 자격 증명 모음에 등록 된 모든 서버 보기</span><span class="sxs-lookup"><span data-stu-id="06975-115">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="06975-116">첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06975-116">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="06975-117">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-117">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="06975-118">두 번째 명령은 $Vault의 자격 증명 모음에서 Windows 형식의 모든 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06975-118">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="06975-119">예제 2: 특정 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="06975-119">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="06975-120">이 명령은 DPMSERVER 이라는 컨테이너를 가져옵니다. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="06975-120">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="06975-121">명령은 $Vault 및 컨테이너 유형의 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-121">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="06975-122">예제 3: 등록 된 모든 Azure 가상 컴퓨터 보기</span><span class="sxs-lookup"><span data-stu-id="06975-122">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="06975-123">이 명령은 $Vault의 자격 증명 모음에서 등록 된 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06975-123">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="06975-124">변수</span><span class="sxs-lookup"><span data-stu-id="06975-124">PARAMETERS</span></span>

### <span data-ttu-id="06975-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06975-125">-DefaultProfile</span></span>
<span data-ttu-id="06975-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="06975-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06975-127">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06975-127">-ManagedResourceGroupName</span></span>
<span data-ttu-id="06975-128">컨테이너와 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-128">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="06975-129">이 이름은 Register-AzureRmBackupContainer cmdlet의 *ServiceName* 또는 *ResourceGroupName* 매개 변수에 대해 지정한 값과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-129">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="06975-130">-이름</span><span class="sxs-lookup"><span data-stu-id="06975-130">-Name</span></span>
<span data-ttu-id="06975-131">이 cmdlet이 가져오는 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-131">Specifies the name of the container that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06975-132">-상태</span><span class="sxs-lookup"><span data-stu-id="06975-132">-Status</span></span>
<span data-ttu-id="06975-133">이 cmdlet이 가져오는 컨테이너의 현재 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-133">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="06975-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="06975-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06975-135">NotRegistered 됨</span><span class="sxs-lookup"><span data-stu-id="06975-135">NotRegistered</span></span> 
- <span data-ttu-id="06975-136">되어</span><span class="sxs-lookup"><span data-stu-id="06975-136">Registered</span></span> 
- <span data-ttu-id="06975-137">등록</span><span class="sxs-lookup"><span data-stu-id="06975-137">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-138">-Type</span><span class="sxs-lookup"><span data-stu-id="06975-138">-Type</span></span>
<span data-ttu-id="06975-139">이 cmdlet이 가져오는 컨테이너의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-139">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06975-140">-저장실</span><span class="sxs-lookup"><span data-stu-id="06975-140">-Vault</span></span>
<span data-ttu-id="06975-141">이 cmdlet이 컨테이너를 가져오는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-141">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="06975-142">**AzureRmBackupVault** 을 얻으려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-142">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06975-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06975-143">CommonParameters</span></span>
<span data-ttu-id="06975-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06975-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06975-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06975-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06975-146">입력</span><span class="sxs-lookup"><span data-stu-id="06975-146">INPUTS</span></span>

### <span data-ttu-id="06975-147">AzureRMBackupVault를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="06975-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="06975-148">매개 변수: 자격 증명 모음 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="06975-148">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="06975-149">출력</span><span class="sxs-lookup"><span data-stu-id="06975-149">OUTPUTS</span></span>

### <span data-ttu-id="06975-150">AzureRMBackupContainer를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="06975-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>

## <span data-ttu-id="06975-151">상속자</span><span class="sxs-lookup"><span data-stu-id="06975-151">NOTES</span></span>
* <span data-ttu-id="06975-152">않아야</span><span class="sxs-lookup"><span data-stu-id="06975-152">None</span></span>

## <span data-ttu-id="06975-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06975-153">RELATED LINKS</span></span>

[<span data-ttu-id="06975-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="06975-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="06975-155">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="06975-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="06975-156">등록 취소-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="06975-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


