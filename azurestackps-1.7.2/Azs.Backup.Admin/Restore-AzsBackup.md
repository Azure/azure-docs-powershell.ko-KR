---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/19/2020
ms.locfileid: "93879930"
---
# <span data-ttu-id="b7898-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="b7898-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="b7898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7898-102">SYNOPSIS</span></span>
<span data-ttu-id="b7898-103">백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-103">Restore a backup.</span></span>

## <span data-ttu-id="b7898-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7898-104">SYNTAX</span></span>

### <span data-ttu-id="b7898-105">Backups_Restore (기본값)</span><span class="sxs-lookup"><span data-stu-id="b7898-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7898-106">리소스</span><span class="sxs-lookup"><span data-stu-id="b7898-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7898-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b7898-107">DESCRIPTION</span></span>
<span data-ttu-id="b7898-108">백업을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-108">Restore a backup.</span></span>

## <span data-ttu-id="b7898-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b7898-109">EXAMPLES</span></span>

### <span data-ttu-id="b7898-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7898-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="b7898-111">Azure 스택 백업에서 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="b7898-112">변수</span><span class="sxs-lookup"><span data-stu-id="b7898-112">PARAMETERS</span></span>

### <span data-ttu-id="b7898-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7898-113">-AsJob</span></span>
<span data-ttu-id="b7898-114">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="b7898-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="b7898-116">암호 해독 인증서의 비밀 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-116">Password of the decryption cert.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="b7898-117">-DecryptionCertPath</span></span>
<span data-ttu-id="b7898-118">개인 키 (.pfx)를 사용 하 여 암호 해독 인증서 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-118">Path to the decryption cert file with private key (.pfx).</span></span>

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

### <span data-ttu-id="b7898-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b7898-119">-Force</span></span>
<span data-ttu-id="b7898-120">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-121">-위치</span><span class="sxs-lookup"><span data-stu-id="b7898-121">-Location</span></span>
<span data-ttu-id="b7898-122">백업할 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b7898-123">-Name</span></span>
<span data-ttu-id="b7898-124">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7898-125">-ResourceGroupName</span></span>
<span data-ttu-id="b7898-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7898-127">-ResourceId</span></span>
<span data-ttu-id="b7898-128">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b7898-129">-Confirm</span></span>
<span data-ttu-id="b7898-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7898-131">-WhatIf</span></span>
<span data-ttu-id="b7898-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7898-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7898-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7898-134">CommonParameters</span></span>
<span data-ttu-id="b7898-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7898-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7898-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7898-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7898-137">입력</span><span class="sxs-lookup"><span data-stu-id="b7898-137">INPUTS</span></span>

## <span data-ttu-id="b7898-138">출력</span><span class="sxs-lookup"><span data-stu-id="b7898-138">OUTPUTS</span></span>

## <span data-ttu-id="b7898-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b7898-139">NOTES</span></span>

## <span data-ttu-id="b7898-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7898-140">RELATED LINKS</span></span>
