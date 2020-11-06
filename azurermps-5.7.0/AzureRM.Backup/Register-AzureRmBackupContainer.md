---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 71c7d883994897e4dc4b450391fb50949a125c77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533735"
---
# <span data-ttu-id="e0977-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e0977-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="e0977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0977-102">SYNOPSIS</span></span>
<span data-ttu-id="e0977-103">백업 자격 증명 모음을 사용 하 여 컨테이너를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0977-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0977-104">SYNTAX</span></span>

### <span data-ttu-id="e0977-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="e0977-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0977-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="e0977-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0977-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e0977-107">DESCRIPTION</span></span>
<span data-ttu-id="e0977-108">**AzureRmBackupContainer** Cmdlet은 Azure Backup 자격 증명 모음을 사용 하 여 컨테이너를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="e0977-109">Azure 백업을 사용 하 여 백업을 구성 하려면 먼저 백업 자격 증명 모음에 서버 또는 가상 컴퓨터를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="e0977-110">이 cmdlet은 지정 된 자격 증명 모음을 사용 하 여 인프라를 서비스 (IaaS) 가상 컴퓨터로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="e0977-111">Register 작업은 Azure 가상 컴퓨터를 백업 자격 증명 모음과 연결 하 고 백업 수명 주기를 통해 가상 컴퓨터를 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="e0977-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e0977-112">EXAMPLES</span></span>

### <span data-ttu-id="e0977-113">예제 1: 백업 자격 증명 모음에 가상 컴퓨터 등록</span><span class="sxs-lookup"><span data-stu-id="e0977-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="e0977-114">첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="e0977-115">명령이 $Vault 변수에 자격 증명 모음을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="e0977-116">두 번째 명령은 Contoso03Vm 이라는 가상 컴퓨터를 $Vault의 자격 증명 모음으로 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="e0977-117">해당 가상 머신이 ContosoService27 이라는 서비스에 속해 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="e0977-118">변수</span><span class="sxs-lookup"><span data-stu-id="e0977-118">PARAMETERS</span></span>

### <span data-ttu-id="e0977-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0977-119">-DefaultProfile</span></span>
<span data-ttu-id="e0977-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e0977-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0977-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e0977-121">-Name</span></span>
<span data-ttu-id="e0977-122">이 cmdlet이 등록 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-122">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0977-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0977-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0977-124">가상 컴퓨터에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-124">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0977-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e0977-125">-ServiceName</span></span>
<span data-ttu-id="e0977-126">이 cmdlet이 등록 하는 가상 컴퓨터의 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-126">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="e0977-127">일반적으로 클라우드 서비스 이름의 접미사는 cloudapp.net입니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-127">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="e0977-128">이 매개 변수를 지정할 때는 접미사를 포함 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="e0977-128">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="e0977-129">가상 컴퓨터에 대 한 정보를 얻으려면 Get-AzureRMVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-129">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="e0977-130">서비스 이름은 가상 컴퓨터 개체의 **Deploymentname** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-130">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0977-131">-저장실</span><span class="sxs-lookup"><span data-stu-id="e0977-131">-Vault</span></span>
<span data-ttu-id="e0977-132">이 cmdlet이 가상 컴퓨터를 등록 하는 백업 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-132">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="e0977-133">**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0977-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0977-134">CommonParameters</span></span>
<span data-ttu-id="e0977-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0977-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0977-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0977-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0977-137">입력</span><span class="sxs-lookup"><span data-stu-id="e0977-137">INPUTS</span></span>

### <span data-ttu-id="e0977-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e0977-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="e0977-139">출력</span><span class="sxs-lookup"><span data-stu-id="e0977-139">OUTPUTS</span></span>

### <span data-ttu-id="e0977-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="e0977-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="e0977-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e0977-141">NOTES</span></span>

## <span data-ttu-id="e0977-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0977-142">RELATED LINKS</span></span>

[<span data-ttu-id="e0977-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e0977-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


