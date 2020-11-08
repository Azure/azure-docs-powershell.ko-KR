---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045530"
---
# <span data-ttu-id="70ec7-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="70ec7-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="70ec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="70ec7-103">특정 가상 컴퓨터에서 SQL Server IaaS 에이전트의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="70ec7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70ec7-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="70ec7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70ec7-105">DESCRIPTION</span></span>
<span data-ttu-id="70ec7-106">**AzureVMSqlServerExtension** cmdlet은 특정 가상 컴퓨터의 IAAS (SQL Server 인프라 as Services) 에이전트 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="70ec7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70ec7-107">EXAMPLES</span></span>

### <span data-ttu-id="70ec7-108">예제 1: 가상 컴퓨터에서 SQL Server 확장의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="70ec7-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="70ec7-109">특정 가상 컴퓨터에서 SQL Server 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="70ec7-110">예제 2: 가상 컴퓨터에서 SQL Server IaaS 에이전트의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="70ec7-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="70ec7-111">파이프 입력을 사용 하 여 특정 가상 컴퓨터에서 SQL Server IaaS 에이전트의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="70ec7-112">예제 3: 가상 컴퓨터에서 특정 SQL Server 버전 IaaS 에이전트의 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="70ec7-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="70ec7-113">이 명령은 가상 컴퓨터에서 특정 버전의 SQL Server IaaS 에이전트에 대 한 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="70ec7-114">변수</span><span class="sxs-lookup"><span data-stu-id="70ec7-114">PARAMETERS</span></span>

### <span data-ttu-id="70ec7-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="70ec7-115">-InformationAction</span></span>
<span data-ttu-id="70ec7-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="70ec7-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70ec7-118">하기로</span><span class="sxs-lookup"><span data-stu-id="70ec7-118">Continue</span></span>
- <span data-ttu-id="70ec7-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="70ec7-119">Ignore</span></span>
- <span data-ttu-id="70ec7-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="70ec7-120">Inquire</span></span>
- <span data-ttu-id="70ec7-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="70ec7-121">SilentlyContinue</span></span>
- <span data-ttu-id="70ec7-122">중지가</span><span class="sxs-lookup"><span data-stu-id="70ec7-122">Stop</span></span>
- <span data-ttu-id="70ec7-123">대기</span><span class="sxs-lookup"><span data-stu-id="70ec7-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ec7-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="70ec7-124">-InformationVariable</span></span>
<span data-ttu-id="70ec7-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ec7-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="70ec7-126">-Profile</span></span>
<span data-ttu-id="70ec7-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="70ec7-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="70ec7-129">-VM</span><span class="sxs-lookup"><span data-stu-id="70ec7-129">-VM</span></span>
<span data-ttu-id="70ec7-130">이 cmdlet에서 설정을 가져오는 영구 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70ec7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ec7-131">CommonParameters</span></span>
<span data-ttu-id="70ec7-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70ec7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ec7-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ec7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ec7-134">입력</span><span class="sxs-lookup"><span data-stu-id="70ec7-134">INPUTS</span></span>

## <span data-ttu-id="70ec7-135">출력</span><span class="sxs-lookup"><span data-stu-id="70ec7-135">OUTPUTS</span></span>

## <span data-ttu-id="70ec7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="70ec7-136">NOTES</span></span>

## <span data-ttu-id="70ec7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70ec7-137">RELATED LINKS</span></span>

[<span data-ttu-id="70ec7-138">제거-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="70ec7-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="70ec7-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="70ec7-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


